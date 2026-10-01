---
description: "Scrolling region with the kit's own thin tracks, which fade out when nothing is happening."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/scrollbar/README.md"
---

import ThemedImage from '@theme/ThemedImage';

import APITable from '@site/src/components/APITable/APITable';

# Scrollbar

Scrolling region with the kit's own thin tracks, which fade out when nothing is happening. It
is what [`Aside`](../overlays/aside.md) and [`DropDown`](../overlays/drop-down.md) put their
content in.

<ThemedImage alt="Scrollbar" width={311} sources={{ light: require('./scrollbar-light.png').default, dark: require('./scrollbar-dark.png').default }} />

## Use this when / not when

- Use for a region of your own that scrolls and should look like the rest of the portal: a
  panel's body, a long list, a dialog's content.
- Not for the page itself. The component needs a parent with a height, and the browser's own
  scrollbar is the right one for the document.
- Not around a virtualised list of your own — [`InfiniteLoader`](../status-components/infinite-loader.md)
  brings its own, and nesting two scrolling regions makes both awkward.
- Not to hide a scrollbar. `noScrollY` stops the content scrolling; it does not hide an
  overflow.

## Import

```ts
import { Scrollbar } from "@onlyoffice/apps-ui-kit/components/scrollbar";
```

Also exported from the root barrel `@onlyoffice/apps-ui-kit`.

Needs `ThemeProvider` from `@onlyoffice/apps-ui-kit/providers/theme` for the thumb's colours,
which differ between the light and the dark theme.

## Minimal example

The scrolling element takes the height of its parent, so the parent is where the height goes.

```tsx
import { Scrollbar } from "@onlyoffice/apps-ui-kit/components/scrollbar";

export function MemberList({ names }: { names: string[] }) {
  return (
    <div style={{ height: 320 }}>
      <Scrollbar>
        {names.map((name) => (
          <p key={name} style={{ margin: "8px 16px" }}>
            {name}
          </p>
        ))}
      </Scrollbar>
    </div>
  );
}
```

## Props


<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `autoFocus`? | `boolean` | Set focus on scroll content element after first render |
| `autoHide`? | `boolean` | Whether the tracks fade out again three seconds after the last scroll or pointer move. Default: `true`. |
| `children`? | `ReactNode` | The content to scroll. |
| `className`? | `string` | Applied to the outermost element. |
| `contentRef`? | `RefObject<HTMLDivElement \| null>` | Ref to access the DOM element of Scroll content element |
| `createContext`? | `boolean` | Publishes the scrollbar on a React context for the components inside it. |
| `fixedSize`? | `boolean` | Fix scrollbar size. Default: `false`. |
| `id`? | `string` | Applied to the outermost element. |
| `noScrollX`? | `boolean` | Stops the content scrolling horizontally. |
| `noScrollY`? | `boolean` | Stops the content scrolling vertically. |
| `onScroll`? | `UIEventHandler<HTMLDivElement>` | Called as the content scrolls, with the native event. |
| `paddingAfterLastItem`? | `string` | Add padding bottom to scroll-body |
| `paddingInlineEnd`? | `string` | Add custom padding-inline-end to scroll-body. |
| `ref`? | `Ref<ScrollbarType \| null>` | Ref to access the DOM element or React component instance |
| `rtl`? | `boolean` | Which side the vertical track is on. It follows the interface direction unless set. |
| `scrollBodyClassName`? | `string` | This class will be placed on scroller body element |
| `scrollClass`? | `string` | This class will be placed on scroller element |
| `style`? | `CSSProperties` | Applied to the outermost element. |
| `tabIndex`? | `null \| number` | Position of the scrolling element in the tab order. The default of -1 keeps it off the tab order, so the region cannot be scrolled with the arrow keys; `null` removes the attribute entirely. Default: `-1`. |
| `translateContentSizesToHolder`? | `boolean` | Both at once. |
| `translateContentSizeXToHolder`? | `boolean` | The same on the horizontal axis. |
| `translateContentSizeYToHolder`? | `boolean` | Gives the outer element the content's own height, so the scrollbar grows with its content instead of filling its parent. |

</APITable>

## Recipes

### A region the keyboard can scroll

`tabIndex` is -1 by default, which keeps the region out of the tab order and so out of reach of
the arrow keys. Pass 0 when the content is long enough to matter.

```tsx
import { Scrollbar } from "@onlyoffice/apps-ui-kit/components/scrollbar";

export function TermsOfUse({ text }: { text: string }) {
  return (
    <div style={{ height: 240 }}>
      <Scrollbar tabIndex={0} autoHide={false}>
        <p style={{ margin: 16 }}>{text}</p>
      </Scrollbar>
    </div>
  );
}
```

### Growing with its content instead of filling its parent

```tsx
import { Scrollbar } from "@onlyoffice/apps-ui-kit/components/scrollbar";

export function ShortList({ names }: { names: string[] }) {
  return (
    <Scrollbar translateContentSizeYToHolder style={{ maxHeight: 200 }}>
      {names.map((name) => (
        <p key={name} style={{ margin: "8px 16px" }}>
          {name}
        </p>
      ))}
    </Scrollbar>
  );
}
```

## Behaviour the types don't state

- **It needs a parent with a height.** The scrolling element fills its parent, so a
  `Scrollbar` in a box of automatic height has nothing to scroll.
  `translateContentSizeYToHolder` is the way round it, together with a `max-height`.
- **The tracks are hidden until something happens.** With `autoHide` — the default — they
  appear on a scroll or a pointer move and fade three seconds later. `autoHide={false}` keeps
  them, which is kinder for a region a user has to read.
- **The markup is three nested elements**: `.scroll-wrapper`, then `.scroller`, then
  `.scroll-body`. Other parts of the kit find the scrolling element by exactly that path — the
  [`InfiniteLoader`](../status-components/infinite-loader.md) looks for
  `#sectionScroll .scroll-wrapper > .scroller` — so give the outer element an id rather than
  restructuring the inside.
- **`paddingAfterLastItem` and `paddingInlineEnd` are written as custom properties in an
  effect**, and only when they are truthy: clearing either one leaves the last value in place.
- `contentRef` is filled in by the ref setter rather than forwarded, so it is available after
  mount, not during render.
- `rtl` follows the interface direction when you leave it out; in a right-to-left interface
  the vertical track moves to the left edge.
- **The thumb thickens on desktop.** From 1024px up it widens from 4px to 8px while the pointer
  is over its track or the thumb is pressed. `fixedSize` keeps it at 8px there all the time;
  below 1024px both stay at `--scrollbar-thumb-size`.
- The scrollbar is the vendored `react-scrollbars-custom`, configured by the kit; `ref` gives
  you its instance, with `scrollTop`, `scrollTo` and the element handles.

## CSS variables

| Variable                         | Default    | Effect                                                                                           |
| -------------------------------- | ---------- | ------------------------------------------------------------------------------------------------ |
| `--scrollbar-bg`                 | theme grey | Colour of the thumb                                                                              |
| `--scrollbar-bg-hover`           | theme grey | Colour of the thumb on hover                                                                     |
| `--scrollbar-bg-active`          | theme grey | Colour of the thumb while dragged                                                                |
| `--scrollbar-thumb-size`         | `4px`      | Thickness of the thumb: its width on the vertical track, its height on the horizontal one        |
| `--scrollbar-radius`             | `8px`      | Corner radius of the track                                                                       |
| `--scrollbar-track-padding`      | `4px`      | Gap between the track's edges and the thumb                                                      |
| `--scrollbar-padding-end`        | `17px`     | Space between the content and the side the vertical track is on; `paddingInlineEnd` overrides it |
| `--scrollbar-padding-end-mobile` | `8px`      | The same space on screens up to 600px wide; `paddingInlineEnd` overrides it too                  |
| `--scrollbar-last-padding`       | unset      | Space after the last item, also a prop                                                           |

The track itself is transparent, so `--scrollbar-radius` shows only where it clips a thumb that
reaches the track's corner — with `--scrollbar-track-padding: 0`.

## Accessibility

- The scrolling element's `tabIndex` is -1, so a keyboard user cannot focus the region and
  cannot scroll it with the arrow keys. Pass `tabIndex={0}` for any region with content worth
  reading, and give it an `aria-label` through the wrapper.
- Nothing here announces that the region scrolls; the tracks are decoration, drawn with
  `<div>`s.
- `autoHide` hides the only visual cue that there is more below. Turn it off when that cue
  matters.

## Test ids

| Element               | `data-testid` |
| --------------------- | ------------- |
| The outermost element | `scrollbar`   |
| The scrolling element | `scroller`    |
| The content element   | `scroll-body` |

None of them can be overridden by a prop.

## Related

- [`Aside`](../overlays/aside.md) — wraps its children in one of these unless told not to.
- [`DropDown`](../overlays/drop-down.md) — uses one for a list with a `maxHeight`.
- [`InfiniteLoader`](../status-components/infinite-loader.md) — the virtualised list, which looks for this
  component's inner elements by class.
