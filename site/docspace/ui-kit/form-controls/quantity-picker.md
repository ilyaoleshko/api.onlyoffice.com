---
description: "Minus and plus around a number, with an optional slider and quick-add chips."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/quantity-picker/README.md"
---

import ThemedImage from '@theme/ThemedImage';

import APITable from '@site/src/components/APITable/APITable';

# QuantityPicker

Minus and plus around a number, with an optional slider and quick-add chips. It is the portal's
"how many users" control, and the number can be typed as well as stepped.

<ThemedImage alt="QuantityPicker" width={790} sources={{ light: require('./quantity-picker-light.png').default, dark: require('./quantity-picker-dark.png').default }} />

## Use this when / not when

- Use for a count the user adjusts up and down — seats, licences, copies — especially where a
  slider or preset increments help.
- Not for an arbitrary number. The control is built around a minimum, a maximum and a step;
  [`TextInput`](./text-input.md) is simpler for a free number.
- Not for a rough value on a continuous range — [`Slider`](./slider.md) alone is that.
- Not for a value that has no bounds. `minValue`, `maxValue` and `step` are all required.

## Import

```ts
import QuantityPicker from "@onlyoffice/apps-ui-kit/components/quantity-picker";
```

It is a **default** export, so the name is yours to choose. The root barrel carries it by name
as well — `components/index.ts` re-exports it as `export { default as QuantityPicker }` — but prefer the
subpath: the barrel does not build without four optional peers, see
[Which import form](../getting-started/installation.md#which-import-form).

Needs `ThemeProvider` from `@onlyoffice/apps-ui-kit/providers/theme`.

## Minimal example

The control is fully controlled: hold the number and set it from `onChange`.

```tsx
import { useState } from "react";
import QuantityPicker from "@onlyoffice/apps-ui-kit/components/quantity-picker";

export function Seats() {
  const [seats, setSeats] = useState(5);

  return (
    <QuantityPicker
      title="Users"
      value={seats}
      minValue={1}
      maxValue={100}
      step={1}
      onChange={setSeats}
    />
  );
}
```

## Props


<APITable>

| Property | Type | Description |
| --- | --- | --- |
| `maxValue` | `number` | Upper bound; nothing the component does goes past it, except the one overflow step `showPlusSign` allows |
| `minValue` | `number` | Lower bound for the controls, typed input and slider |
| `onChange` | `(value: number) => void` | Called with the new value |
| `step` | `number` | Amount the plus and minus controls and the slider move by; the last step up is shortened so it stops at the bound |
| `value` | `number` | Current value; the component is controlled |
| `className`? | `string` | Class name on the root element |
| `decreaseLabel`? | `string` | Accessible name of the minus control, e.g. a translated "Decrease"; no `aria-label` is rendered without it |
| `disableValue`? | `string` | Text shown in place of the value while `isDisabled` is set; the field then sizes to its content |
| `enableZero`? | `boolean` | Allows zero as a value below `minValue`; other values below it are flagged |
| `increaseLabel`? | `string` | Accessible name of the plus control, e.g. a translated "Increase"; no `aria-label` is rendered without it |
| `isDisabled`? | `boolean` | Disables every control and replaces the input with static text |
| `isLarge`? | `boolean` | Widens the value field from 101px to 140px |
| `isZeroAllowed`? | `boolean` | **Deprecated.** Use `enableZero`. |
| `items`? | `(number \| TabItemObject)[]` | Preset tabs; selecting one adds its amount to the current value, capped like the plus control |
| `minusDisabled`? | `boolean` | Disables only the minus control; it stays focusable (`aria-disabled`) so `minusTooltipId` can still explain why |
| `minusTooltipId`? | `string` | Tooltip id set as `data-tooltip-id` on the minus control |
| `showPlusSign`? | `boolean` | Lets the value go exactly one past `maxValue` (to `maxValue + 1`), shown as `maxValue+` |
| `showSlider`? | `boolean` | Renders a slider bound to the value, from `minValue` to `maxValue` (`maxValue + 1` with `showPlusSign`) |
| `subtitle`? | `string` | Secondary line under the title; omitted when empty |
| `title`? | `null \| string` | Heading above the controls; omitted when empty |
| `underControlsTitle`? | `React.ReactNode` | Text under the controls; turns to the warning colour while an invalid value is entered with `enableZero` |
| `withoutControls`? | `boolean` | Hides the plus and minus controls |

</APITable>

## Recipes

### Disabled / read-only

`isDisabled` replaces the field with plain text, so nothing can be typed or focused.
`disableValue` is what that text says when the number itself is not the right thing to show.

```tsx
import QuantityPicker from "@onlyoffice/apps-ui-kit/components/quantity-picker";

export function FixedSeats({ seats }: { seats: number }) {
  return (
    <QuantityPicker
      title="Users"
      value={seats}
      minValue={1}
      maxValue={100}
      step={1}
      isDisabled
      disableValue="Set by your plan"
      onChange={() => {}}
    />
  );
}
```

### A slider and quick-add chips

`items` are **increments**, not values: a chip labelled `+10` adds ten to whatever is there.

```tsx
import { useState } from "react";
import QuantityPicker from "@onlyoffice/apps-ui-kit/components/quantity-picker";

export function SeatsWithPresets() {
  const [seats, setSeats] = useState(10);

  return (
    <QuantityPicker
      title="Users"
      subtitle="Billed monthly"
      value={seats}
      minValue={1}
      maxValue={250}
      step={1}
      showSlider
      showPlusSign
      items={[10, 50, { name: "100", value: 100 }]}
      underControlsTitle={`${seats} users`}
      onChange={setSeats}
    />
  );
}
```

## Behaviour the types don't state

- **Typing is held as a draft and committed on blur or Enter.** Until then `onChange` fires for
  each valid intermediate number, but an empty field is not reported — it settles to 0 or
  `minValue` when you leave it.
- **Out-of-range typing is treated unevenly.** A number above `maxValue` is replaced at once by
  the cap (`maxValue`, or `maxValue + 1` with `showPlusSign`) and reported straight away. A
  number below `minValue` is not reported while you type; on blur or Enter it is raised to
  `minValue` — or, with `enableZero`, kept exactly as typed and flagged.
- **Non-digits are stripped as you type**, so a minus sign or a decimal point cannot be entered
  at all; the control is whole, non-negative numbers only.
- **`showPlusSign` changes what the maximum means.** Above `maxValue` the display becomes
  `<maxValue>+`, typing a larger number reports `maxValue + 1`, and the slider's own maximum is
  `maxValue + 1` so the handle can reach that overflow step.
- **The slider writes its bounds at its ends**: `minValue` at the start and `maxValue` at the
  end, followed by `+` with `showPlusSign`.
- **`items` add, they do not set.** A chip's number is added to the current value, and the chips
  never look selected — they are buttons, not a choice.
- **The minus button stops at `minValue`, or at 0 with `enableZero`.** With `enableZero` a value
  between 0 and `minValue` also turns the line under the controls into its warning colour, and
  plus from anywhere below `minValue` jumps straight to `minValue` rather than adding `step`.
- **`underControlsTitle` always renders**, even when empty, so the control reserves that line's
  height whether or not you use it.
- **`isDisabled` removes the field from the DOM**, replacing it with text — so refs, focus and
  test queries against the input stop working while it is disabled.
- `minusDisabled` disables only the minus button; `minusTooltipId` puts `data-tooltip-id` on it
  for a [`Tooltip`](../overlays/tooltip.md) you render yourself.
- `isZeroAllowed` is the former name of `enableZero` and still works as an alias:
  `enableZero ?? isZeroAllowed ?? false`, so `enableZero` wins when both are set. It is marked
  deprecated; write `enableZero` in new code.

## CSS variables

The control is styled from the shared theme tokens rather than custom properties of its own.
The slider inside follows [`Slider`](./slider.md).

## Accessibility

- **The plus and minus controls are real `<button type="button">`s**, so they are in the tab
  order and answer Enter and Space. Tab reaches minus, the number and plus in that order. Their
  icons are `aria-hidden`, so they are unnamed until you pass `decreaseLabel` and
  `increaseLabel` — no `aria-label` is rendered without them, and a screen reader then announces
  two nameless buttons.
- `minusDisabled` leaves the minus control focusable and marks it `aria-disabled`, so a tooltip
  attached through `minusTooltipId` can still be read; only `isDisabled` sets the real
  `disabled`.
- The number is a [`TextInput`](./text-input.md) given `tabIndex={0}` by the component,
  against the kit's own default of `-1`. It has no label; name it through your own markup, and
  note it disappears entirely when `isDisabled`.
- The quick-add chips are [`TabItem`](../navigation/tab-item.md)s, which present as tabs rather than
  as buttons that change a number.
- The slider is a real range input and is the only part fully usable from the keyboard — see
  [`Slider`](./slider.md), which has no visible focus ring of its own.
- Nothing announces the minimum, the maximum or that a value was clamped.

## Test ids

| Element          | `data-testid`                |
| ---------------- | ---------------------------- |
| The field        | `quantity_picker_input`      |
| The minus button | `quantity_picker_minus_icon` |
| The plus button  | `quantity_picker_plus_icon`  |
| The slider       | `quantity_picker_slider`     |
| A quick-add chip | `add_<value>_tab_item`       |

None of them can be overridden by a prop.

## Related

- [`Slider`](./slider.md) — the slider it can show, and the control for a rough value.
- [`TextInput`](./text-input.md) — the field in the middle.
- [`TabItem`](../navigation/tab-item.md) — what the quick-add chips are built from.
