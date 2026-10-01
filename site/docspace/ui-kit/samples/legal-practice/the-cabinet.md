---
custom_edit_url: "https://github.com/ONLYOFFICE/docspace-ui-kit-react/blob/master/docs/samples/legal/cabinet/Cabinet.mdx"
---

import ThemedImage from '@theme/ThemedImage';

# The cabinet

The whole application, in one story. A lawyer opens it and gets the firm's
matters; a client opens it and gets theirs. Open a matter, and it is the
checklist from the previous screens. Everything after this page is a part
of it, taken out to be looked at on its own.

<ThemedImage alt="Default" width={795} sources={{ light: require('./the-cabinet--default-light.png').default, dark: require('./the-cabinet--default-dark.png').default }} />

With no portal the frame runs on demo data, for both people. Connect a portal
from the **API** control in the toolbar and **As the lawyer** is the key
owner's real workspace; register the OAuth app in
[Who is signed in](./setup/who-is-signed-in.md)
and **As the client** signs a client in as themselves.

## Assembled, not written

The frame adds no screen of its own. It holds:

| Part                | From                                                                                  | What it is here                                             |
| ------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `MattersBody`       | [01. My matters](./screens/my-matters.md)              | the list, with a click on a matter that opens it            |
| `MatterRoomPanel`   | [02. Inside a matter](./screens/inside-a-matter.md)    | the opened matter: checklist, drafts, facts                 |
| `ClientSession`     | [Who is signed in](./setup/who-is-signed-in.md)   | the client's sign-in, and the provider that holds their token |
| `useMattersView`    | below                                                                                 | who is reading and what they may see, demo already resolved |

Which screen is showing is the only state a shell has. Here it is a value in
`useState`, so the story needs no router. In an application it is the URL:
`NavMenu` takes a `LinkRouter`, and every entry with `linkData` becomes the
router's link. The screens themselves do not change, because none of them
knows how it was reached.

<ThemedImage alt="Source" width={851} sources={{ light: require('./the-cabinet--block0-light.png').default, dark: require('./the-cabinet--block0-dark.png').default }} />

## The shell

- **`NavMenu`** is the sidebar: one group, the list of matters with a count
  badge, and the open matter as a second entry while there is one. It owns
  which section is expanded and nothing else; what is active and what a click
  does come from the frame.
- **`Avatar`** at the bottom draws the reader's picture, fetched through
  `usePortalImage` because the path the portal gives is protected, or their
  initials when there is none.
- **`Tabs`** above the frame switch between the two people. That is the
  story's control, not the application's: a real deployment serves one
  frame, and knows which from the token it holds.
- The two-column layout is the sample's own: a grid of a 240px sidebar and
  the page, which stacks on a phone.

## What lands here next

Each later screen is added to the frame in the commit that adds the screen:
sending a document from the checklist, reading a draft in the editor, and
opening a matter from the workspace.

## The code

<ThemedImage alt="Source" width={851} sources={{ light: require('./the-cabinet--block1-light.png').default, dark: require('./the-cabinet--block1-dark.png').default }} />
