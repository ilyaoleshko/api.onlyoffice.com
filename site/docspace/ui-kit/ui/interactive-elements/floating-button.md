---
description: "Round corner badge that shows the progress of a background operation and opens its panel."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/floating-button/README.md"
---

import ThemedImage from '@theme/ThemedImage';

import APITable from '@site/src/components/APITable/APITable';

# FloatingButton

Round corner badge that shows the progress of a background operation and opens its panel. It is
the disc that appears in the bottom corner of the portal while files are uploading.

<ThemedImage alt="FloatingButton" width={71} sources={{ light: require('./floating-button-light.png').default, dark: require('./floating-button-dark.png').default }} />

## Use this when / not when

- Use for one long operation running in the background — an upload, a conversion, a bulk move —
  that the user should be able to watch and come back to.
- Not for the progress of a single row; [`LoadingButton`](../feedback/loading-button.md) is the
  16px version that sits inline.
- Not for a determinate bar inside a panel — [`ProgressBar`](../status-components/progress-bar.md) is that.
- Not for a primary action floating over the content: this one is a status badge, and its
  colour is fixed to the accent.

## Import

```ts
import { FloatingButton } from "@onlyoffice/apps-ui-kit/components/floating-button";
```

Also exported from the root barrel `@onlyoffice/apps-ui-kit`.

Needs `ThemeProvider` from `@onlyoffice/apps-ui-kit/providers/theme`, and specifically its
colour scheme: the circle's background is the accent colour, and without one it has no
background at all unless you pass `color`.

## Minimal example

The component positions itself against the nearest positioned ancestor — see "Behaviour the
types don't state".

```tsx
import { FloatingButton } from "@onlyoffice/apps-ui-kit/components/floating-button";

export function UploadBadge({
  percent,
  onOpen,
}: {
  percent: number;
  onOpen: () => void;
}) {
  return (
    <div style={{ position: "relative", height: 200 }}>
      <FloatingButton icon="upload" percent={percent} onClick={onOpen} />
    </div>
  );
}
```

## Props


<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `alert`? | `boolean` | Whether the badge shows the warning triangle. `stopped` wins over it. Default: `false`. |
| `className`? | `string` | Applied to the circle, after the component's own classes. |
| `clearUploadedFilesHistory`? | `() => void` | Called when the cancel cross is clicked. |
| `color`? | `string` | CSS colour of the circle and of the progress ring. Without it the accent colour is used. |
| `completed`? | `boolean` | Whether the operation is finished: the ring fades out and the circle pulses once. Default: `false`. |
| `icon`? | `"arrow" \| "backup" \| "copy" \| "deletePermanently" \| "dots" \| "download" \| "duplicate" \| "exportIndex" \| "markAsRead" \| …` | Which of the built-in icons is drawn in the middle. Ignored when `iconUrl` is set. Default: `"other"`. |
| `iconUrl`? | `string` | URL of an image to draw instead of the built-in icon, at 20px wide. |
| `id`? | `string` | Applied to the circle, not to the wrapper that positions it. |
| `onClick`? | `(e: React.MouseEvent) => void` | Called with the event when the circle is clicked. The cancel cross has its own handler. |
| `percent`? | `number` | How much of the ring is filled, 0–100. Without it the ring spins instead. |
| `showCancelButton`? | `boolean` | Whether the cancel cross exists at all. It is only visible on hover unless `showCloseIcon` is set. |
| `showCloseIcon`? | `boolean` | Whether that cross stays visible without hovering. |
| `stopped`? | `boolean` | Shows the "stopped" status icon: the operation was aborted by the user. Takes precedence over `alert` and `completed`. Default: `false`. |
| `style`? | `CSSProperties` | Applied to the circle as inline style. |
| `withoutProgress`? | `boolean` | Whether the progress ring is left out entirely, leaving the bare circle. |
| `withoutStatus`? | `boolean` | Whether the status badge is suppressed whatever `stopped`, `alert` and `completed` say. Default: `false`. |

</APITable>

#### Added by the wrapper the folder exports

The `index` module exports a wrapped component, so these are accepted on top of the props above.

<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `ref`? | `Ref<HTMLDivElement>` | Allows getting a ref to the component instance. Once the component unmounts, React will set `ref.current` to `null` (or call the ref with `null` if you passed a callback ref). |

</APITable>

`icon` is a key of `FloatingButtonIcons`, which is exported beside the component:
`upload`, `trash`, `move`, `duplicate`, `plus`, `minus`, `refresh`, `exportIndex`, `dots`,
`arrow`, `deletePermanently`, `download`, `copy`, `markAsRead`, `other`, `backup`.

## Recipes

### Finished

`completed` fades the ring out, plays a one-off brightening of the circle and turns the badge
into a tick.

```tsx
import { FloatingButton } from "@onlyoffice/apps-ui-kit/components/floating-button";

export function UploadDone({ onOpen }: { onOpen: () => void }) {
  return (
    <div style={{ position: "relative", height: 200 }}>
      <FloatingButton icon="upload" completed onClick={onOpen} />
    </div>
  );
}
```

### Failed or aborted

`alert` draws the warning triangle and `stopped` the "aborted" mark, which wins over both
`alert` and `completed`.

```tsx
import { FloatingButton } from "@onlyoffice/apps-ui-kit/components/floating-button";

export function UploadFailed({ onOpen }: { onOpen: () => void }) {
  return (
    <div style={{ position: "relative", height: 200 }}>
      <FloatingButton icon="upload" alert completed onClick={onOpen} />
    </div>
  );
}
```

### Cancellable

`showCancelButton` adds a cross beside the circle, which calls `clearUploadedFilesHistory`. It
only appears on hover unless `showCloseIcon` keeps it out.

```tsx
import { FloatingButton } from "@onlyoffice/apps-ui-kit/components/floating-button";

export function CancellableUpload({
  percent,
  onOpen,
  onCancel,
}: {
  percent: number;
  onOpen: () => void;
  onCancel: () => void;
}) {
  return (
    <div style={{ position: "relative", height: 200 }}>
      <FloatingButton
        icon="upload"
        percent={percent}
        onClick={onOpen}
        showCancelButton
        clearUploadedFilesHistory={onCancel}
      />
    </div>
  );
}
```

## Behaviour the types don't state

- **The component positions itself.** From the desktop breakpoint up its wrapper is
  `position: absolute`, 100×70, pinned to the bottom trailing corner of the nearest positioned
  ancestor, at `z-index: 300`; the circle inside it is `z-index: 500`. Give it a
  `position: relative` parent, or it will pin itself to something further up the page.
- **The background is `!important` and comes from the theme's colour scheme.** Without a colour
  scheme — and without `color` — the declaration resolves to nothing and the circle is drawn
  transparent, icon and ring floating on the page.
- **`percent` does not complete the operation.** The finished look is controlled by `completed`
  alone; `percent={100}` keeps the ring and the running look until you pass it.
- **Without `percent` the ring spins.** The indeterminate animation is the default, and a
  `percent` above 0 replaces it with an arc of that share.
- **`withoutProgress` removes the ring, not the animation** — the circle is drawn on its own,
  and `percent` then has nothing to show.
- **The cancel cross lives outside the circle**, 77px from the trailing edge and 33px from the
  bottom of the wrapper, and fades in on hover. On a device with no hover it is invisible
  unless `showCloseIcon` is set. Its handler is `clearUploadedFilesHistory`, not `onClick`.
- **`showCancelButton` and `showCloseIcon` are two different switches.** The first decides
  whether the cross exists; the second whether it is visible without hovering.
- **The status badge has a fixed precedence**: `stopped`, then `alert`, then `completed`.
  `withoutStatus` suppresses all three.
- **`iconUrl` is rendered as a plain `<img width={20}>`** with `alt="icon"`, so it is not
  recoloured by the theme the way the built-in icons are.
- **`id`, `className` and `style` go on the circle, not on the wrapper** that carries the
  position — so `className` cannot be used to move the button.
- The circle is 48px, the ring 38px and the icon box 38px. There is no size prop, and
  `--floating-button-button-size` only resizes the clickable disc — see "CSS variables".

## CSS variables

Set them on any ancestor.

| Variable                              | Default       | Effect                                                                                        |
| ------------------------------------- | ------------- | --------------------------------------------------------------------------------------------- |
| `--floating-circle-button-background` | accent colour | Circle and progress ring colour, and the fill of the accent icons' shapes.                    |
| `--floating-button-button-size`       | `48px`        | Width and height of the clickable circle only; the ring and the icon stay 48px in its corner. |
| `--floating-button-icon`              | theme token   | Fill of the icon, except the accent icons.                                                    |
| `--floating-button-shadow`            | theme shadow  | Whole `box-shadow` of the circle.                                                             |

The accent icons are `upload`, `trash`, `deletePermanently` and `other`: their shapes are painted
in the circle's colour, so `--floating-button-icon` does not reach them.

`--floating-button-button-size` resizes nothing but the clickable disc — the ring, the icon box
and the status badge are laid out in a fixed 48px box in its top corner, so any other value puts
them out of line with it.

`color` writes the first of these inline, so it wins over an ancestor's value.

## Accessibility

- **The circle is a `<div>` with a click handler.** It carries `data-role="button"` — an
  attribute, not the `role` — so assistive technology sees a plain element, and there is no
  `tabIndex` or key handler to reach it with.
- `aria-label` is set to the icon's name followed by the word "button" (`"upload button"`), in
  **English regardless of the interface language**, and cannot be overridden.
- The progress is conveyed only by the ring: no `role="progressbar"`, no `aria-valuenow`, so
  the percentage is invisible to a screen reader.
- An `iconUrl` image is announced by its `alt`, which is always `"icon"`.
- The cancel cross is an SVG with a click handler and no name of its own. Anything cancellable
  needs a real control elsewhere as well.

## Test ids

| Element          | `data-testid`                                               |
| ---------------- | ----------------------------------------------------------- |
| The circle       | `floating-button`                                           |
| The ring         | `floating-button-progress`                                  |
| The status badge | `floating-button-alert`                                     |
| Its icon         | `floating-button-stopped-icon`, `-alert-icon`, `-tick-icon` |
| The cancel cross | `floating-button-close-icon`                                |
| The main icon    | `icon-<name>`, e.g. `icon-upload`                           |

None of them can be overridden by a prop.

## Related

- [`LoadingButton`](../feedback/loading-button.md) — the same idea at 16px, inline in a row.
- [`ProgressBar`](../status-components/progress-bar.md) — the linear form of the same number.
- [`OperationsProgressButton`](https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/operations-progress-button/README.md) — the portal's panel
  this badge opens.
