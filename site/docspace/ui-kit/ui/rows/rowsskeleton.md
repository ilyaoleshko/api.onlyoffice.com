---
description: "Placeholder in the shape of a list of rows, shown while the rows themselves are loading. The Rows page describes it in full."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/rows/skeletons/RowsSkeleton.stories.tsx"
---

import ThemedImage from '@theme/ThemedImage';

# RowsSkeleton

Placeholder in the shape of a list of rows, shown while the rows themselves are loading. The Rows page describes it in full.

<ThemedImage alt="RowsSkeleton" width={790} sources={{ light: require('./rowsskeleton--primary-light.png').default, dark: require('./rowsskeleton--primary-dark.png').default }} />

## Props

<ThemedImage alt="RowsSkeleton props" width={851} sources={{ light: require('./rowsskeleton--controls-light.png').default, dark: require('./rowsskeleton--controls-dark.png').default }} />

## Stories

### Default

Five placeholder rows (`count`) with the band sweeping across them, as a list shows them while its first page loads. Change any other prop live in the Controls panel below.

<ThemedImage alt="Default" width={790} sources={{ light: require('./rowsskeleton--default-light.png').default, dark: require('./rowsskeleton--default-dark.png').default }} />

### Static Placeholder

A placeholder that does not move, for a reader who asked for less motion: the band no longer sweeps across the shapes (`animate`). The component does not check the system's reduced-motion setting itself.

<ThemedImage alt="Static Placeholder" width={790} sources={{ light: require('./rowsskeleton--static-placeholder-light.png').default, dark: require('./rowsskeleton--static-placeholder-dark.png').default }} />

### Round Start Element

Rows for a list of people, whose start element is a round avatar: each `RowSkeleton` draws a circle in place of the square (`isRectangle={false}`). `RowsSkeleton` has no such prop, so a list of round rows is built from `RowSkeleton` directly.

<ThemedImage alt="Round Start Element" width={790} sources={{ light: require('./rowsskeleton--round-start-element-light.png').default, dark: require('./rowsskeleton--round-start-element-dark.png').default }} />
