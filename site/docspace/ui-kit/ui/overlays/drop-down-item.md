---
description: "One row of a dropdown menu: a label, an optional icon and badges, or a separator."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/drop-down-item/README.md"
---

import ThemedImage from '@theme/ThemedImage';

import APITable from '@site/src/components/APITable/APITable';

# DropDownItem

One row of a dropdown menu: a label, an optional icon and badges, or a separator. It is what
[`DropDown`](./drop-down.md) expects its children to be.

<ThemedImage alt="DropDownItem" width={94} sources={{ light: require('./drop-down-item-light.png').default, dark: require('./drop-down-item-dark.png').default }} />

## Use this when / not when

- Use inside a [`DropDown`](./drop-down.md), a
  [`ContextMenu`](./context-menu.md) or a [`ComboBox`](../form-controls/combobox.md)'s list —
  anywhere a menu row is needed.
- Not on its own as a button or a list row: it is a `<div>` with `role="option"`, which is
  wrong outside a menu. [`Button`](../interactive-elements/button.md) or a row of your own is the honest
  choice there.
- Not for a checkbox row of a form. `withToggle` exists for a setting inside a menu, not for a
  form control — that is [`ToggleButton`](../form-controls/toggle-button.md) in a
  [`FieldContainer`](../form-controls/field-container.md).

## Import

```ts
import { DropDownItem } from "@onlyoffice/apps-ui-kit/components/drop-down-item";
```

Also exported from the root barrel `@onlyoffice/apps-ui-kit`.

Needs `ThemeProvider` from `@onlyoffice/apps-ui-kit/providers/theme` for the text, hover and
icon colours, and `TranslationProvider` from `@onlyoffice/apps-ui-kit/providers/translation` for
the default text of the paid badge — pass `paidLabel` if you would rather not depend on it.

## Minimal example

```tsx
import { DropDownItem } from "@onlyoffice/apps-ui-kit/components/drop-down-item";

export function RenameItem({ onRename }: { onRename: () => void }) {
  return <DropDownItem label="Rename" onClick={onRename} />;
}
```

## Props


<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `additionalElement`? | `ReactNode` | Additional element to render at the end of the item, after all other content |
| `badgeLabel`? | `string` | Text of the paid badge, used instead of the translated default. |
| `betaLabel`? | `string` | Text of the beta badge, used instead of the host's own constant. |
| `checked`? | `boolean` | Whether the toggle switch is in a checked state |
| `children`? | `ReactNode` | Content of the item, used **instead of** `label` — it is rendered only when `label` is empty, not alongside it. `additionalElement` is the one that comes after the label. |
| `className`? | `string` | CSS class name to apply to the root element for custom styling |
| `description`? | `ReactNode` | Secondary line rendered under the item label and always visible - what choosing this item means. The item grows to fit it. |
| `disabled`? | `boolean` | Stops `onClick` firing and greys the item out. The enclosing `DropDown` also drops disabled items from its list unless `showDisabledItems` is set. Default: `false`. |
| `externalLinkPath`? | `string` | URL to navigate to when the external link icon is clicked |
| `fillIcon`? | `boolean` | Whether the icon should be filled with the current text color. If false, uses original icon colors. Default: `true`. |
| `headerArrowAction`? | `() => void` | Callback function triggered when the header's back arrow is clicked |
| `height`? | `number` | Height the enclosing `DropDown` reserves for this item in its virtualised list, in pixels. It does not style the item — the row is 32px tall until you also set `--drop-down-item-height` — and it reaches the DOM as an attribute. |
| `heightTablet`? | `number` | The same, used instead of `height` on a tablet-width viewport. |
| `icon`? | `ComponentClass<any, any> \| FunctionComponent<any> \| ReactElement<unknown, string \| JSXElementConstructor<any>> \| string` | Icon at the start of the item. A component or element is rendered as given; a string is a URL — a path containing `.svg` or `images/` is fetched and inlined, anything else becomes an `<img>`. |
| `id`? | `string` | HTML ID attribute for the root element |
| `isActive`? | `boolean` | Whether the item is in an active/pressed state. Default: `false`. |
| `isActiveDescendant`? | `boolean` | Whether the item is the current active descendant for keyboard navigation |
| `isBeta`? | `boolean` | Whether to show a beta badge next to the item |
| `isHeader`? | `boolean` | Whether to render the item as a header with special styling. Default: `false`. |
| `isModern`? | `boolean` | Whether to use modern compact styling with minimal padding |
| `isPaidBadge`? | `boolean` | Whether to show a paid badge next to the item |
| `isSelected`? | `boolean` | Whether the item is currently selected in a menu context |
| `isSeparator`? | `boolean` | Whether to render the item as a separator line instead of content. Default: `false`. |
| `isSubMenu`? | `boolean` | Whether this item opens a submenu when clicked. Default: `false`. |
| `label`? | `ReactNode` | Primary text content or React node to display in the item. Default: `""`. |
| `minWidth`? | `string` | Sets minimum width for the root element |
| `noActive`? | `boolean` | Whether to disable the active/pressed state styling. Default: `false`. |
| `noHover`? | `boolean` | Whether to disable the hover state styling. Default: `false`. |
| `onClick`? | `(e: React.MouseEvent<HTMLElement> \| React.ChangeEvent<HTMLInputElement>) => void` | Called on a click on the item, and on a change of the toggle when `withToggle` is set — hence the event union. It is not called while the item is disabled. |
| `onClickSelectedItem`? | `() => void` | Callback function triggered when a selected item is clicked |
| `onExternalLinkClick`? | `() => void` | Callback triggered when the external link icon is clicked |
| `onMouseDown`? | `(e: React.MouseEvent<HTMLElement>) => void` | Callback function triggered on mouse down |
| `paidLabel`? | `string` | Text of the paid badge, used instead of the translated default. |
| `setOpen`? | `(open: boolean) => void` | Called with `false` after every click, disabled ones included, for the enclosing menu to close itself. |
| `stopMouseDownPropagation`? | `boolean` | When true, stops mousedown propagation to prevent click-outside detection from closing dropdown before click fires |
| `style`? | `CSSProperties` | Inline CSS styles to apply to the root element |
| `tabIndex`? | `number` | Position in the tab order. The default of -1 keeps the item off it. Default: `-1`. |
| `testId`? | `string` | Value of `data-testid` on the item. Default: `"drop-down-item"`. |
| `textOverflow`? | `boolean` | Whether text content should be truncated with ellipsis when it overflows. Default: `false`. |
| `tooltip`? | `string` | Hint shown when the item is disabled, on a touch device only. It needs `RootTooltip` mounted, and it does nothing on an enabled item or with a pointer. |
| `truncateText`? | `boolean` | Whether to apply additional text truncation styling to the label |
| `withExternalLink`? | `boolean` | Whether to show an external link icon at the end of the item |
| `withHeaderArrow`? | `boolean` | Whether to show a back arrow icon when item is a header |
| `withoutIcon`? | `boolean` | Whether to hide the icon element even when an icon prop is provided. Default: `false`. |
| `withToggle`? | `boolean` | Whether to show a toggle switch at the end of the item |

</APITable>

## Recipes

### Disabled, with a separator above it

A separator is its own item, and the enclosing menu drops one that ends up first or last.

```tsx
import { DropDownItem } from "@onlyoffice/apps-ui-kit/components/drop-down-item";

export function DeleteSection({
  canDelete,
  onDelete,
}: {
  canDelete: boolean;
  onDelete: () => void;
}) {
  return (
    <>
      <DropDownItem isSeparator />
      <DropDownItem
        label="Delete for ever"
        disabled={!canDelete}
        tooltip="Only the room owner can delete it"
        onClick={onDelete}
      />
    </>
  );
}
```

### A setting with a toggle, and a second line

`description` renders under the label and makes the row taller — tell the enclosing menu about
it with `height`.

```tsx
import { useState } from "react";
import { DropDownItem } from "@onlyoffice/apps-ui-kit/components/drop-down-item";

export function NotificationsItem() {
  const [on, setOn] = useState(false);

  return (
    <DropDownItem
      label="Notify me"
      description="Send an email whenever a file changes"
      withToggle
      checked={on}
      height={56}
      onClick={() => setOn(!on)}
    />
  );
}
```

### A nested level: a header with a way back

A submenu level opens with a header row; `withHeaderArrow` puts a back arrow before its title.

```tsx
import { DropDownItem } from "@onlyoffice/apps-ui-kit/components/drop-down-item";

export function SharingLevel({
  onBack,
  onCopyLink,
}: {
  onBack: () => void;
  onCopyLink: () => void;
}) {
  return (
    <>
      <DropDownItem
        isHeader
        withHeaderArrow
        headerArrowAction={onBack}
        label="Sharing"
      />
      <DropDownItem label="Copy link" onClick={onCopyLink} />
    </>
  );
}
```

## Behaviour the types don't state

- **`children` replaces the label, it does not follow it.** The item renders `label` if there is
  one and `children` only when there is not. Content after the label is `additionalElement`.
- **`height` and `heightTablet` do not resize the item.** They are read by
  [`DropDown`](./drop-down.md) to lay out its virtualised list; the row itself is 32px
  of line height until you also set `--drop-down-item-height`. Get them out of step and the rows
  overlap or leave gaps. They also reach the DOM as attributes, since the component spreads what
  it does not read.
- **A disabled item still closes the menu.** `onClick` is skipped, but `setOpen(false)` is
  called on every click regardless.
- **Every string label gets a hover tooltip.** The label is wrapped in the kit's
  `TooltipContainer` with the label as its title, so it needs
  [`RootTooltip`](./tooltip.md) mounted to show anything — and nothing appears if you
  have not mounted it.
- **`tooltip` is for disabled items on touch devices only.** With a pointer, or on an enabled
  item, it does nothing at all.
- An icon given as a string is resolved by its path: one containing `.svg` or `images/` is
  fetched by `react-svg` and inlined, a data URL likewise, and anything else becomes an `<img>`
  with the hard-coded alt text `plugin-logo`.
- A separator renders a non-breaking space and a border, and the enclosing menu reserves 12px
  for it (16 on a tablet) rather than the usual 32.
- `isHeader` also turns off the hover and active styling, whatever `noHover` and `noActive` say.
- **`isSubMenu` only draws a trailing arrow.** It opens nothing by itself — the enclosing menu
  does that from `onClick`. The arrow turns downwards while `isActive` is set and is mirrored in
  a right-to-left interface.
- **`isActive` and `isSelected` do different jobs.** `isActive` paints the selected background;
  `isSelected` only sets `aria-selected` and routes a click to `onClickSelectedItem` — on every
  click of a selected item, a disabled one included — and paints the background only when the
  item is also disabled.
- **The row clips a long label but shows no ellipsis on its own**, because it is a flex row.
  `truncateText` puts the ellipsis on the label, and `textOverflow` makes the whole row a block
  so its own ellipsis applies.

## CSS variables

| Variable                            | Default    | Effect                                                                  |
| ----------------------------------- | ---------- | ----------------------------------------------------------------------- |
| `--drop-down-item-height`           | `32px`     | Line height of the row                                                  |
| `--drop-down-item-padding`          | `0 12px`   | Padding inside the row                                                  |
| `--drop-down-item-font-size`        | `13px`     | Size of the label                                                       |
| `--drop-down-item-font-weight`      | `600`      | Weight of the label, a header's included                                |
| `--drop-down-item-color`            | theme text | Colour of the label                                                     |
| `--drop-down-item-disabled-color`   | theme grey | Colour of a disabled item's label                                       |
| `--drop-down-item-hover-bg`         | theme grey | Background on hover, while pressed and on the keyboard-highlighted item |
| `--drop-down-item-icon-fill`        | theme icon | Colour of a filled icon, a disabled item's included                     |
| `--drop-down-item-divider`          | theme line | Colour of a separator and of the line under a header                    |
| `--drop-down-item-header-height`    | `48px`     | Height of a header row                                                  |
| `--drop-down-item-header-font-size` | `15px`     | Size of a header's text                                                 |

On a tablet-width viewport the row ignores `--drop-down-item-height` and `--drop-down-item-padding`:
its line height is `36px` and its padding `0 16px` regardless.

`--drop-down-min-width` is written by the component from the `minWidth` prop.

## Accessibility

- The row is a `<div role="option">` — or `role="separator"` — with `aria-selected` and
  `aria-disabled`, but its parent is a `role="listbox"` that is not linked to any control, so
  the pattern is incomplete on its own.
- **`tabIndex` is -1 by default, and that is correct here**, unlike on the kit's inputs: an
  option inside a listbox is meant to stay off the tab order while the container keeps focus and
  the arrow keys move a highlight. That is the active-descendant pattern: the menu sets
  `isActiveDescendant` on the highlighted row, which paints it and sets `data-focused`. What is
  incomplete is the container, per the point above — not this. The arrow keys also work only when the menu has a `maxHeight`.
- Clicks are handled on the row, and there is no key handler: Enter and Space do nothing unless
  the enclosing menu's keyboard navigation is on.
- The badges are text inside the row, so their meaning is announced; the external-link icon is
  not labelled.

## Test ids

| Element  | `data-testid`                               |
| -------- | ------------------------------------------- |
| The item | `drop-down-item`, overridable with `testId` |

## Related

- [`DropDown`](./drop-down.md) — the menu this belongs in, and where `height` is read.
- [`ContextMenu`](./context-menu.md) — the menu that opens at the pointer.
- [`ComboBox`](../form-controls/combobox.md) — builds its list out of these.
