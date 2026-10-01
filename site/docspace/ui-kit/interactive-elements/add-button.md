---
description: "Square icon button with an optional label beside it, for adding one more of something."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/add-button/README.md"
---

import ThemedImage from '@theme/ThemedImage';

import APITable from '@site/src/components/APITable/APITable';

# AddButton

Square icon button with an optional label beside it, for adding one more of something. It is
the "add members" affordance of the portal's selectors: a 32px tile with a plus in it.

<ThemedImage alt="AddButton" width={48} sources={{ light: require('./add-button-light.png').default, dark: require('./add-button-dark.png').default }} />

## Use this when / not when

- Use for adding an item to a list the user is building — a member, a tag, a share.
- Not for a form's submit or a dialog's action; [`Button`](./button.md) has the sizes
  and the primary look.
- Not for an icon action with no "add" meaning — [`IconButton`](./icon-button.md) is
  the bare icon.
- Not for choosing from a prepared list, which is what [`Selector`](../overlays/selector.md) is
  for; this is the button that opens one.

## Import

```ts
import { AddButton } from "@onlyoffice/apps-ui-kit/components/add-button";
```

Also exported from the root barrel `@onlyoffice/apps-ui-kit`.

Needs `ThemeProvider` from `@onlyoffice/apps-ui-kit/providers/theme`. It reads the colour
scheme directly, not only the theme class — `isAction` and `size` do nothing without one.

## Minimal example

`tabIndex` is what makes the button focusable; it has no default.

```tsx
import { AddButton } from "@onlyoffice/apps-ui-kit/components/add-button";

export function AddMember({ onAdd }: { onAdd: () => void }) {
  return <AddButton label="Add member" tabIndex={0} onClick={onAdd} />;
}
```

## Props


<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `className`? | `string` | Applied to the wrapper that holds the square and the label. |
| `dir`? | `"auto" \| "ltr" \| "rtl"` | Writing direction of the label. |
| `fontSize`? | `string` | Font size of the label, as a CSS length. Default: `"13px"`. |
| `iconName`? | `string` | URL of the icon, fetched at runtime. Ignored when `iconNode` is set; without either, a plus is drawn. |
| `iconNode`? | `ReactNode` | Icon element to draw instead of the plus. |
| `iconSize`? | `number` | Size of the icon inside the square, in pixels. Default: `12`. |
| `id`? | `string` | Applied to the square, not to the wrapper. |
| `isAction`? | `boolean` | Whether the square is tinted with the accent colour instead of grey. It needs a colour scheme from the theme. |
| `isDisabled`? | `boolean` | Whether the button is inert: the icon greys out, the label dims and clicks are dropped. Default: `false`. |
| `isLoading`? | `boolean` | Whether a spinner replaces the icon and clicks are dropped. Default: `false`. |
| `label`? | `string` | Text drawn after the square. Without it the button is the square alone. |
| `lineHeight`? | `string` | Line height of the label, as a CSS length. Default: `"20px"`. |
| `noSelect`? | `boolean` | Whether the label cannot be selected with the pointer. |
| `onClick`? | `(e: React.MouseEvent) => void` | Called with the event when the square or the label is clicked, and on Enter when the wrapper has focus. |
| `size`? | `string` | Side of the square, as a CSS length. It only takes effect when the theme supplies a colour scheme. |
| `style`? | `CSSProperties` | Applied to the square as inline style. |
| `tabIndex`? | `number` | `tabIndex` of the wrapper. Without it the button cannot be focused, and the Enter handler never runs. |
| `testId`? | `string` | `data-testid` of the square. Default: `"selector-add-button"`. |
| `title`? | `string` | Tooltip shown on hover, through the kit's own tooltip rather than the browser's. |
| `titleText`? | `string` | `title` attribute of the label — the browser's own tooltip, unlike `title`. |
| `truncate`? | `boolean` | Whether the label is truncated with an ellipsis instead of wrapping. |

</APITable>

## Recipes

### Loading

`isLoading` swaps the icon for a spinner and drops the click. The square keeps its size, so the
row does not jump.

```tsx
import { AddButton } from "@onlyoffice/apps-ui-kit/components/add-button";

export function AddMemberPending({
  pending,
  onAdd,
}: {
  pending: boolean;
  onAdd: () => void;
}) {
  return (
    <AddButton
      label="Add member"
      tabIndex={0}
      isLoading={pending}
      onClick={onAdd}
    />
  );
}
```

### Disabled / read-only

`isDisabled` greys the icon, dims the label and stops the click — including the Enter key.

```tsx
import { AddButton } from "@onlyoffice/apps-ui-kit/components/add-button";

export function AddMemberLocked() {
  return <AddButton label="Add member" isDisabled onClick={() => {}} />;
}
```

### An icon of your own

`iconNode` replaces the plus with any element; `iconName` takes a **URL** instead, which the
kit fetches at runtime.

```tsx
import { AddButton } from "@onlyoffice/apps-ui-kit/components/add-button";

export function AddTag({ onAdd }: { onAdd: () => void }) {
  return (
    <AddButton
      label="New tag"
      tabIndex={0}
      onClick={onAdd}
      iconSize={16}
      iconNode={
        <svg viewBox="0 0 16 16" aria-hidden="true">
          <path d="M8 3v10M3 8h10" stroke="currentColor" strokeWidth="1.5" />
        </svg>
      }
    />
  );
}
```

## Behaviour the types don't state

- **Keyboard support is opt-in.** The wrapper carries `role="button"` and an Enter handler, but
  **no `tabIndex` unless you pass one** — without it the button cannot be focused and the
  handler never runs. Enter is ignored while `isDisabled` or `isLoading` is set, and Space
  does nothing in either case.
- **`isAction` needs a colour scheme, not just a theme.** The accent tint is written as an
  inline custom property from the theme's `currentColorScheme.main.accent`; when the provider
  has none, that property is never set and the rule
  `background-color: var(--main-accent-button) !important` leaves the square transparent.
- **`size` shares that fate.** It is only written when the colour scheme exists, so under a
  provider without one the square stays 32×32 whatever you pass.
- **`title` is the kit's tooltip, `titleText` is the browser's.** The first goes through the
  tooltip wrapper and is drawn by the kit on hover; the second is a plain `title` attribute on
  the label.
- **`id` and `style` land on the square**, not on the wrapper, while `className` lands on the
  wrapper — the three are not applied to the same element.
- **The label is part of the click target.** It is a [`Text`](../data-display/text.md) with the same
  handler, so clicking the words adds too.
- **The square is 32×32 with 10px of padding**, and the icon inside it defaults to 12px, so a
  larger `iconSize` eats into the padding rather than growing the square.
- **The wrapper is `display: flex` with no gap**; the label's 8px of spacing is its own
  `padding-inline-start`, from `--add-button-text-gap`.
- **`truncate` needs a bounded parent.** It sets `min-width: 0` on the wrapper and lets the
  label ellipsis, which only shows up when something upstream limits the width.
- Without `iconNode` **and** without `iconName` the default plus is drawn — the button is never
  empty.

## CSS variables

Set them on any ancestor.

| Variable                         | Default     | Effect                                                            |
| -------------------------------- | ----------- | ----------------------------------------------------------------- |
| `--add-button-dimension`         | `32px`      | Side of the square; the `size` prop wins over it.                 |
| `--add-button-radius`            | `3px`       | Corner radius of the square.                                      |
| `--add-button-bg`                | theme grey  | Background of the square.                                         |
| `--add-button-bg-hover`          | theme token | Background while hovered.                                         |
| `--add-button-bg-active`         | theme token | Background while pressed.                                         |
| `--add-button-icon-color`        | theme token | Fill of the icon.                                                 |
| `--add-button-icon-color-hover`  | theme token | Fill of the icon while the pointer is on the square around it.    |
| `--add-button-icon-color-active` | theme token | Fill of the icon while pressed, with the same limit as the hover. |
| `--add-button-text-gap`          | `8px`       | Space between the square and the label.                           |
| `--add-button-text-disabled`     | theme grey  | Label colour while disabled.                                      |

- **`isAction` and `isDisabled` override the square's colours.** Under `isAction` the
  background and the icon take the accent colour, and while disabled the theme's own greys
  are forced with `!important`, so `--add-button-bg` and `--add-button-icon-color` (and their
  hover and pressed forms) no longer apply. `--add-button-text-disabled` is the only variable
  that survives the disabled state.
- **The icon's hover fill only shows around the icon.** With the pointer over the icon itself,
  [`IconButton`](./icon-button.md)'s own hover colour is the more specific rule and
  wins over `--add-button-icon-color-hover` and `--add-button-icon-color-active`.

## Accessibility

- The wrapper is a `<div role="button">` with an Enter handler. That is enough for a screen
  reader to announce it as a button **only if you pass `tabIndex`**; Space still does nothing,
  which a real button would handle.
- **There is no accessible name unless you provide one.** `label` is rendered as ordinary text
  inside the same wrapper, so it does name the button — but a button without `label` has none,
  and `title` does not supply it.
- `aria-disabled` is not set. A disabled button is still announced as an ordinary button; only
  the click and the Enter key are dropped.
- The icon square itself is an [`IconButton`](./icon-button.md) inside the wrapper,
  which is a `<div>` with no role of its own.

## Test ids

| Element     | `data-testid`                      |
| ----------- | ---------------------------------- |
| The wrapper | `selector-add-button-container`    |
| The square  | `selector-add-button`, or `testId` |

Only the square's id can be overridden, through `testId` rather than `dataTestId`.

## Related

- [`IconButton`](./icon-button.md) — the icon alone, with no tile behind it.
- [`Button`](./button.md) — the full-size button with a label inside it.
- [`Selector`](../overlays/selector.md) — the list this button usually opens.
