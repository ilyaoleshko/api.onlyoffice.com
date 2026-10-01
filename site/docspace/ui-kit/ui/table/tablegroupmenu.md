---
description: "TableGroupMenu is the toolbar that takes the place of the table header while rows are selected, with a select-all checkbox and the actions that apply to the selection.\n\nThe Table README describes it in full."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/table/table-group-menu/TableGroupMenu.stories.tsx"
---

import ThemedImage from '@theme/ThemedImage';

# TableGroupMenu

TableGroupMenu is the toolbar that takes the place of the table header while rows are selected, with a select-all checkbox and the actions that apply to the selection.

The Table README describes it in full.

<ThemedImage alt="TableGroupMenu" width={790} sources={{ light: require('./tablegroupmenu--primary-light.png').default, dark: require('./tablegroupmenu--primary-dark.png').default }} />

## Props

<ThemedImage alt="TableGroupMenu props" width={851} sources={{ light: require('./tablegroupmenu--controls-light.png').default, dark: require('./tablegroupmenu--controls-dark.png').default }} />

## Stories

### Default

The toolbar a user sees after selecting rows, with the actions that apply to them; change any other prop live in the Controls panel below.

<ThemedImage alt="Default" width={790} sources={{ light: require('./tablegroupmenu--default-light.png').default, dark: require('./tablegroupmenu--default-dark.png').default }} />

### Checked

Every row is selected, so the checkbox is ticked and a click on it clears the selection (`isChecked`).

<ThemedImage alt="Checked" width={790} sources={{ light: require('./tablegroupmenu--checked-light.png').default, dark: require('./tablegroupmenu--checked-dark.png').default }} />

### Indeterminate

Some rows but not all are selected, so the checkbox is partly ticked and a click on it selects the rest (`isIndeterminate`).

<ThemedImage alt="Indeterminate" width={790} sources={{ light: require('./tablegroupmenu--indeterminate-light.png').default, dark: require('./tablegroupmenu--indeterminate-dark.png').default }} />

### With Header Label

A text in place of the checkbox, for a toolbar that acts on something other than a list of rows the user can select all of (`headerLabel`).

<ThemedImage alt="With Header Label" width={790} sources={{ light: require('./tablegroupmenu--with-header-label-light.png').default, dark: require('./tablegroupmenu--with-header-label-dark.png').default }} />

### Closeable

A cross before the info panel button, for a toolbar the user can dismiss without clearing the selection by hand (`isCloseable`, `onCloseClick`).

<ThemedImage alt="Closeable" width={790} sources={{ light: require('./tablegroupmenu--closeable-light.png').default, dark: require('./tablegroupmenu--closeable-dark.png').default }} />

### Blocked

Every action greyed out and ignoring clicks while an operation on the selection is still running (`isBlocked`); the checkbox stays usable.

<ThemedImage alt="Blocked" width={790} sources={{ light: require('./tablegroupmenu--blocked-light.png').default, dark: require('./tablegroupmenu--blocked-dark.png').default }} />

### Info Panel Open

While the info panel is open, its button at the end is drawn in the accent colour on a round background, so the user sees that a click closes the panel (`isInfoPanelVisible`).

<ThemedImage alt="Info Panel Open" width={790} sources={{ light: require('./tablegroupmenu--info-panel-open-light.png').default, dark: require('./tablegroupmenu--info-panel-open-dark.png').default }} />

### Right To Left

In a right-to-left interface the checkbox moves to the right edge, the actions follow it leftwards and the info panel button sits at the left edge with its icon mirrored.

<ThemedImage alt="Right To Left" width={790} sources={{ light: require('./tablegroupmenu--right-to-left-light.png').default, dark: require('./tablegroupmenu--right-to-left-dark.png').default }} />

### Css Customization

The variable set on a wrapper -- it is listed under CSS variables in the Table README.

<ThemedImage alt="Css Customization" width={790} sources={{ light: require('./tablegroupmenu--css-customization-light.png').default, dark: require('./tablegroupmenu--css-customization-dark.png').default }} />
