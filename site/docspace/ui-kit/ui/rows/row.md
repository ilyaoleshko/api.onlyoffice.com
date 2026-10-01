---
description: "One row of the file list: an optional checkbox, a start element, the content and a context menu."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/rows/row/README.md"
---

import ThemedImage from '@theme/ThemedImage';

import APITable from '@site/src/components/APITable/APITable';

# Row

One row of the file list: an optional checkbox, a start element, the content and a context
menu. Which parts appear is decided by which props you pass at all, not by their values.

<ThemedImage alt="Row" width={783} sources={{ light: require('./row-light.png').default, dark: require('./row-dark.png').default }} />

## Use this when / not when

- Use inside a [`RowContainer`](./row-container.md), with a
  [`RowContent`](./row-content.md) as its child — the shape the portal's file list is
  made of.
- Not as a generic list row. It reads `item` off its child's props to build its context menu's
  header, and it renders a right-click menu whether or not you want one.
- Not for tabular data the user sorts: [`Table`](../table/index.md).
- Not for a clickable card or a menu entry —
  [`DropDownItem`](../overlays/drop-down-item.md) or markup of your own is smaller and says
  what it is.

## Import

```ts
import { Row } from "@onlyoffice/apps-ui-kit/components/rows/row";
```

`components/index.ts` does not list this folder, but it lists `rows`, and `export *`
is transitive — so the name arrives from `@onlyoffice/apps-ui-kit/components/rows` and from
the root barrel `@onlyoffice/apps-ui-kit` as well.

`RowProps` is **not** exported — type a wrapper's props yourself, or import the type from its
file path.

Needs `ThemeProvider` from `@onlyoffice/apps-ui-kit/providers/theme`, and
`TranslationProvider` from `@onlyoffice/apps-ui-kit/providers/translation` for the context
menu's own labels.

## Minimal example

`contextOptions` is what decides whether a context button is rendered; an empty array means no.

```tsx
import { Row } from "@onlyoffice/apps-ui-kit/components/rows/row";
import { RowContent } from "@onlyoffice/apps-ui-kit/components/rows/row-content";
import { Text } from "@onlyoffice/apps-ui-kit/components/text";

export function FileRow({ name }: { name: string }) {
  return (
    <Row contextOptions={[]}>
      <RowContent>
        <Text fontWeight={600}>{name}</Text>
        <span />
      </RowContent>
    </Row>
  );
}
```

## Props


<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `badgesComponent`? | `ReactNode` | Element placed before `contentElement`, for badges of your own. |
| `badgeUrl`? | `string` | URL of the badge image shown in the context menu's header. |
| `checked`? | `boolean` | Whether the row's checkbox is ticked. Its **presence** is what renders the checkbox at all — passing `checked={false}` gives an unticked box, omitting the prop gives none. |
| `children`? | `ReactElement<{ item: RowItemType; }, string \| JSXElementConstructor<any>>` | The row's content, normally a `RowContent`. The row reads `item` off this element's props to build the header of its context menu. |
| `className`? | `string` | Applied to the row element. |
| `contentElement`? | `ReactNode` | Element placed before the context button, after the badges. |
| `contextButtonSpacerWidth`? | `string` | Width reserved for the context button, as a CSS length. Default: `"26px"`. |
| `contextOptions`? | `ContextMenuModel[]` | Items of the context menu. They may be given here or as `data.contextOptions`, which wins; an empty list renders no button. |
| `contextTitle`? | `string` | Hover tooltip of the context button. |
| `data`? | `TData` | Arbitrary payload handed back to `onSelect`. Its `contextOptions`, if it has any, are the ones the menu uses. |
| `dataTestId`? | `string` | Value of `data-testid` on the row. Default: `"row"`. |
| `element`? | `ReactElement<unknown, string \| JSXElementConstructor<any>>` | Element at the start of the row — an avatar or a file icon. Like `checked`, its presence is what reserves the space. |
| `getContextModel`? | `() => ContextMenuModel[]` | Builds the context menu's items when it opens, instead of `contextOptions`. |
| `id`? | `string` | Ignored. Nothing reads this prop and no `id` reaches the DOM. |
| `indeterminate`? | `boolean` | Draws the checkbox as partly ticked, for a group that is half-selected. |
| `inProgress`? | `boolean` | Replaces the checkbox and the start element with a spinner. |
| `isArchive`? | `boolean` | Tells the context menu that the room is archived. |
| `isDisabled`? | `boolean` | Disables the checkbox, and nothing else about the row. |
| `isIndexEditingMode`? | `boolean` | Replaces the context button with the up and down arrows of index editing. |
| `isRoom`? | `boolean` | Tells the context menu that this row is a room, which changes its header. |
| `item`? | `RowItemType` | Ignored. The context menu's header is read from the child's own `item` prop. |
| `mode`? | `TMode` | `modern` moves the checkbox on top of the start element, so it needs both `checked` and `element` to render either. Default: `"default"`. |
| `onChangeIndex`? | `(action: VDRIndexingAction) => void` | Called with the direction when an index arrow is clicked. |
| `onContextClick`? | `(value?: boolean) => void` | Called when the context menu is asked for, with `true` for a right-click. |
| `onRowClick`? | `(e: React.MouseEvent) => void` | Called by a click on the start element and on the content, but not on the checkbox or the context button. |
| `onSelect`? | `(checked: boolean, data?: unknown) => void` | Called with the new checked state and whatever `data` holds. |
| `rowContextClose`? | `() => void` | Called when the context menu closes. |
| `style`? | `CSSProperties` | Ignored. Nothing reads this prop and no inline style reaches the DOM. |
| `withoutBorder`? | `boolean` | Removes the row's bottom border. Default: `false`. |

</APITable>

## Recipes

### Selection

```tsx
import { useState } from "react";
import { Row } from "@onlyoffice/apps-ui-kit/components/rows/row";
import { RowContent } from "@onlyoffice/apps-ui-kit/components/rows/row-content";
import { Text } from "@onlyoffice/apps-ui-kit/components/text";

export function SelectableRow({ name }: { name: string }) {
  const [checked, setChecked] = useState(false);

  return (
    <Row
      checked={checked}
      contextOptions={[]}
      onSelect={(next) => setChecked(next)}
      onRowClick={() => setChecked(!checked)}
    >
      <RowContent>
        <Text fontWeight={600}>{name}</Text>
        <span />
      </RowContent>
    </Row>
  );
}
```

### Loading

`inProgress` replaces the checkbox and the start element with a spinner; the content and the
context menu stay.

```tsx
import { Row } from "@onlyoffice/apps-ui-kit/components/rows/row";
import { RowContent } from "@onlyoffice/apps-ui-kit/components/rows/row-content";
import { Text } from "@onlyoffice/apps-ui-kit/components/text";

export function UploadingRow({ name, done }: { name: string; done: boolean }) {
  return (
    <Row checked={false} inProgress={!done} contextOptions={[]}>
      <RowContent>
        <Text fontWeight={600}>{name}</Text>
        <span />
      </RowContent>
    </Row>
  );
}
```

### Disabled

`isDisabled` disables the checkbox alone. The row stays clickable and its context menu still
opens.

```tsx
import { Row } from "@onlyoffice/apps-ui-kit/components/rows/row";
import { RowContent } from "@onlyoffice/apps-ui-kit/components/rows/row-content";
import { Text } from "@onlyoffice/apps-ui-kit/components/text";

export function LockedRow({ name }: { name: string }) {
  return (
    <Row checked={false} isDisabled contextOptions={[]}>
      <RowContent>
        <Text fontWeight={600}>{name}</Text>
        <span />
      </RowContent>
    </Row>
  );
}
```

## Behaviour the types don't state

- **A prop being present is what renders a part.** The row asks whether `checked`, `element` and
  `contentElement` are keys of its props, not whether they hold anything, so
  `checked={undefined}` still renders a checkbox and omitting the prop is the only way to have
  none.
- **The context menu's header comes from the child's `item` prop.** The row reaches into
  `children.props.item` for the title, icon, avatar and logo — so the header is empty unless the
  child accepts and carries an `item`. The row's own `item` prop is not read at all.
- **Options may come from two places.** `data.contextOptions` wins over `contextOptions` when it
  has any; `getContextModel` is what the menu calls when it opens. With no options the button is
  replaced by an empty spacer of `contextButtonSpacerWidth`.
- **The whole row opens the menu on right-click**, and if the menu is not mounted yet the row
  clicks itself first to mount it — a workaround left in the source.
- **`onRowClick` is bound to the content and the start element**, not to the row: a click on the
  checkbox, the badges or the context button does not reach it.
- On a touch device a click on the start element also selects the row, calling `onSelect(true)`.
- `mode="modern"` puts the checkbox in the start element's place and needs **both** `checked`
  and `element` present, or neither is rendered. The start element shows until the row is
  checked or the pointer is over it; then the checkbox takes its place. The hover swap is off
  on a touch device and in index-editing mode, where only checking the row shows the checkbox.
- On a phone-sized screen the context menu opens behind a backdrop, and a menu taller than
  210px opens as a sheet from the bottom, under the header built from the child's `item`.
- `id` and `style` are declared and never read; `className` is the way in.
- The component is memoised with a deep comparison of all its props.

## Accessibility

- The row is a `<div>` with no role, not focusable, and its click handlers are on inner
  elements. The [`Checkbox`](../form-controls/checkbox.md) is the only part a keyboard reaches.
- The context menu opens on right-click or from a [`ContextMenuButton`](../interactive-elements/context-menu-button.md),
  which is itself a `<div>` — there is no keyboard route to it.
- Nothing announces selection: the row carries no `aria-selected`, only a class.

## Test ids

| Element | `data-testid`                        |
| ------- | ------------------------------------ |
| The row | `row`, overridable with `dataTestId` |

## Related

- [`RowContent`](./row-content.md) — the child this expects, and where `item` lives.
- [`RowContainer`](./row-container.md) — the list around it.
- [`ContextMenu`](../overlays/context-menu.md) — the menu it renders for every row.
