---
description: "Placeholder in the shape of a tile listing, shown while the tiles themselves are loading. The Tiles page describes it in full."
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/components/tiles/sub-components/skeletons/TilesSkeleton.stories.tsx"
---

import ThemedImage from '@theme/ThemedImage';

# TilesSkeleton

Placeholder in the shape of a tile listing, shown while the tiles themselves are loading. The Tiles page describes it in full.

<ThemedImage alt="TilesSkeleton" width={789} sources={{ light: require('./tilesskeleton--primary-light.png').default, dark: require('./tilesskeleton--primary-dark.png').default }} />

## Props

<ThemedImage alt="TilesSkeleton props" width={851} sources={{ light: require('./tilesskeleton--controls-light.png').default, dark: require('./tilesskeleton--controls-dark.png').default }} />

## Stories

### Default

Two folder and four file placeholders under their heading bars (`foldersCount`, `filesCount`), as a tile listing shows them while its first page loads. Change any other prop live in the Controls panel below.

<ThemedImage alt="Default" width={789} sources={{ light: require('./tilesskeleton--default-light.png').default, dark: require('./tilesskeleton--default-dark.png').default }} />

### Files Without Heading

A folder that holds files only and shows no heading above them: no folder placeholders, so their bar goes as well, and no bar above the files (`foldersCount={0}`, `withTitle={false}`).

<ThemedImage alt="Files Without Heading" width={789} sources={{ light: require('./tilesskeleton--files-without-heading-light.png').default, dark: require('./tilesskeleton--files-without-heading-dark.png').default }} />

### Tile Shapes

The three shapes one `TileSkeleton` can take, for a listing that builds its own placeholder grid: a folder bar (`isFolder`), a room card with a logo, a title bar, a small square for the menu and two tag bars (`isRoom`), and a file card. `TilesSkeleton` never draws the room card, so a grid of rooms is built from `TileSkeleton` directly.

<ThemedImage alt="Tile Shapes" width={768} sources={{ light: require('./tilesskeleton--tile-shapes-light.png').default, dark: require('./tilesskeleton--tile-shapes-dark.png').default }} />
