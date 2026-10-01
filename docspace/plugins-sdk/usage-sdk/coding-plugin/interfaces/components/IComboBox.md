---
custom_edit_url: https://github.com/ONLYOFFICE/docspace-plugin-sdk/blob/release/v4.0.0/src/interfaces/components/IComboBox.ts
---

# IComboBox

Custom combo box input.

![combobox](https://ilyaoleshko.github.io/assets/images/docspace/combobox.png#gh-light-mode-only)![combobox](https://ilyaoleshko.github.io/assets/images/docspace/combobox.dark.png#gh-dark-mode-only)

## Example

Multi-language selector with toast notifications

```typescript
const languageSelector: IComboBox = {
  options: [
    {
      key: "en-US",
      label: "English (US)",
      icon: "language-en.svg"
    },
    {
      key: "es-ES",
      label: "Español",
      icon: "language-es.svg"
    },
    {
      key: "fr-FR",
      label: "Français",
      icon: "language-fr.svg",
      disabled: true
    }
  ],
  selectedOption: {
    key: "en-US",
    label: "English (US)",
    icon: "language-en.svg"
  },
  onSelect: (item) => {
    return {
      actions: [Actions.updateProps, Actions.showToast],
      newProps: {
        selectedOption: item
      },
      toastProps: [{
        title: `Interface language changed to ${item.label}`,
        type: ToastType.success
      }]
    };
  },
  scaled: true,
  directionX: "right",
  directionY: "bottom",
  displayType: "default",
  dropDownMaxHeight: 300,
  showDisabledItems: true,
  withBackdrop: true,
  isDisabled: false,
  noBorder: false,
  opened: false,
  scaledOptions: true,
  modernView: true
}
```

## Properties

import APITable from '@site/src/components/APITable/APITable';

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `options` | [`IComboBoxItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IComboBox.md#icomboboxitem)[] | Defines the combo box options |
| `selectedOption` | [`IComboBoxItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IComboBox.md#icomboboxitem) | Defines the combo box selected option |
| `onSelect?` | (`item`: [`IComboBoxItem`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/components/IComboBox.md#icomboboxitem)) => `void` \| [`IMessage`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/utils.md#imessage) | Sets a function which is triggered whenever the combo box is selected |
| `scaled?` | `boolean` | Specifies that the combo box is scaled by its parent |
| `directionX?` | `"left"` \| `"right"` | Defines the position of the combo box in the X direction |
| `directionY?` | `"both"` \| `"top"` \| `"bottom"` | Defines the position of the combo box in the Y direction |
| `displayType?` | `"default"` \| `"toggle"` | Defines the combo box display type |
| `modernView?` | `boolean` | Specifies whether to display the combo box in the modern view |
| `isDisabled?` | `boolean` | Specifies if the combo box is disabled or not |
| `showDisabledItems?` | `boolean` | Whether to show disabled combo box options |
| `opened?` | `boolean` | Specifies whether to open the combo box |
| `scaledOptions?` | `boolean` | Specifies whether the combo box options are scaled by the combo box button |
| `onToggle?` | () => `void` \| [`IMessage`](https://ilyaoleshko.github.io/api.onlyoffice.com/docspace/plugins-sdk/usage-sdk/coding-plugin/interfaces/utils.md#imessage) | Sets a function which is triggered whenever the combo box is clicked when "displayType == toggle" |
| `noBorder?` | `boolean` | Specifies whether to display the combo box without borders |
| `withBackdrop?` | `boolean` | Specifies whether the combo box contains a backdrop |
| `dropDownMaxHeight?` | `number` | Defines the maximum height of the dropdown list |
| `className?` | `string` | Defines the CSS class for styling the component. Can be used to override or extend the default component styles. |

</APITable>

***

## IComboBoxItem

Custom combo box option.

### Example

Basic language option with icon

```typescript
const languageOption: IComboBoxItem = {
  key: "en-US",
  label: "English (US)",
  icon: "language-en.svg",
  disabled: false
}
```

### Properties

<APITable>

| Property | Type | Description |
| ------ | ------ | ------ |
| `key` | `string` | Unique identifier for the option |
| `label` | `string` | Display text for the option |
| `icon?` | `string` | The option display icon. The icon image must be uploaded to the assets folder. Only the image name with the extension must be specified in this field. |
| `disabled?` | `boolean` | Specifies if the combo box option is disabled or not |

</APITable>
