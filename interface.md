# Interface

This page describes all script windows and their functionality.

---

## Main UI

> Interface is as simple as it gets. Each color swatch represents a label color.

![Main UI](./assets/UI/main.svg ':size=800')

- **Target**: and option to select what to target:
  - Keyframes or
  - Layers and/or Project items
- **Filter (F)**: (depending on the *Target*)
  - shows witch labels are used in selected Keyframes or Layers/Items.
  - shows witch labels are unused in selected Keyframes or Layers/Items.
- **Back (B)**: brings all available color swatches to the UI.
- **Reset (X)**: depending on the *Target*, sets Keyframe or Layer/Item default label color.
- **Settings (S)**:
  - opens up the [Settings](#settings) window.
  - SHIFT: opens the [Snippet editor](#snippet-editor) window.
  - CMD: reloads Labels interface. Usefull when labels where changed manually in the `AE > Preferences > Labels` window.
  - ALT: opens `AE > Preferences > Labels` window.
  - ALT + CMD: reveals the *Adobe After Effects \<version> Prefs-indep-general.txt* file where all labels related data is stored.

---

## Settings

![Settings UI](./assets/UI/settings.svg ':size=800')

- Theme:
  - *Dropdown* list contains all installed label themes. By default, theme files are installed inside `/Users/USERNAME/Library/Application Support/aescripts/renderTom/Labels/VERSION/Themes/` folder.
  - **Delete** - deletes theme from the dropdown list.
  - **Export** - exports selected theme from the list.
  - **Import** - imports theme file and adds it to the list.
  - **Save** - opens [save theme](#save-theme) window to save current Label Preferences to the theme file.

- Checkboxes:
  - **Show label name in tooltip** - toggles tooltip visibility.
  - **Show filter buttons** - toggles visibility of **Filter (F)** and **Back (B)** buttons in the Labels UI.
  - **Select locked layers** - toggles locked layer selection.

- Keyboard keys:
  - **Set color** - sets label color.
  - **Affect layer & item** - affects both layer and its source item at once.
  - **Select label group** - selects same label group.
  - **Append to selection** - adds current label group to selection.
  - **Select all except** - selects all label groups except the current one.
  - **Remove from selection** - removes current label group from selection.
  - **Open swatch editor** - opens the [Swatch editor](#swatch-editor) window.

Use modifiers keys (*SHIFT*, *CMD*, *ALT*) and/or a key name (*Q*, *W*, *E*, *R*, *T*, *Y* etc) to set keyboard keys. To mix modifiers and a key name, always use the **+** symbol as a separator: *SHIFT + CMD + E*, *ALT + E*. Character cases and spaces between **+** are ignored: *SHIFT+E* is totally fine.

You can combine multiple modifier keys together, however, only one key name is allowed: i.e. *shift + e + r* or *shift + cmd + e + r* will not work.

- **Open snippet editor** - opens the [Snippet editor](#snippet-editor) window.

---

## Snippet editor

![Snippet editor UI](./assets/UI/snippet-editor.svg ':size=800')

- **Script name**: assigned automatically. Usually it's the base name of the target script file.
- **Key**: a keyboard key to be pressed when clicking on a swatch to execute the target script.
- **Path to script file**: the file path of the targeted script file.

TODO: add a link to Snippets tutorial and downloads

---

## Swatch editor

Swatch editor is an interface for changing label color and name. It can be accessed by *e + click* (corresponds to a key defined in the [settings](#settings) window **Open swatch editor** section) on any of the swatches.

![Swatch editor](./assets/UI/swatch-editor.svg ':size=260')

- **Color**: HEX color code for a label.
- **Name:** the name of the label.

---

## Save theme

![Save theme](./assets/UI/save-theme.svg ':size=260')

- **Name**: the name of the theme.
- **Designer**: designers name, optional.
- **URL**: designers url, optional.
