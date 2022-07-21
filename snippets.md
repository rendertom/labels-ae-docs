# Snippets

Similar to [KBar](https://aescripts.com/kbar/) the Labels script can be used as a script launcher. Simply assign a custom keyboard key and a path to the script and click on swatch to execute the script.

> Snippets opens a gateway to extend Labels functionality and build upon what’s already implemented in the script.

---

## Download

Download all the snippets at once [here](https://github.com/rendertom/Labels/releases/download/assets/Snippets.zip ':ignore') or pick the one you like from the list below.

* [Copy Color To Clipboard](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Copy%20Color%20To%20Clipboard.js) - copies labels HEX color to the clipboard,
* [Create Shape Layer](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Create%20Shape%20Layer.js) - creates a full sized Shape Layer and sets Fill color to the label color,
* [Create Solid Layer](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Create%20Solid%20Layer.js) - creates a full sized Solid Layer and sets its source color to the label color,
* [Group Layers](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Group%20Layers.js) - groups all layers with same label color together underneath the topmost layer with that color,
* [Parent Layers to Null](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Parent%20Layers%20to%20Null.js) - parents all layers with the same label color to a null,
* [Push Layers Back By One](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Push%20Layers%20Back%20By%20One.js) - pushes layers with this label to the bottom of the layer stack one by one,
* [Push Layers Up By One](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Push%20Layers%20Up%20By%20One.js) - pushes layers with this label to the top of the layer stack one by one,
* [Shy Everything Except](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Shy%20Everything%20Except.js) toggles 'solo' property of all layers that do not match given label color in composition,
* [Toggle Shy](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Toggle%20Shy.js) - toggles 'shy' property of all layers with given label color in composition,
* [Toggle Solo](https://raw.githubusercontent.com/rendertom/Labels/master/Snippets/Toggle%20Solo.js) - toggles 'shy' property of all layers with given label color in composition.

---

## How to create

Labels script exposes the following API:

``` javascript
index (Number)            // label index,
hex (String)              // label HEX color,
rgb ([Number])            // label RGB color [0-255, 0-255, 0-255]
name (String)             // label name
targetKeyframes (Boolean) // whether the target:keyframes is enabled in the main UI
```

The example below demonstrates how to create a simple snippet for Labels.

```javascript
// Get an active composition
var composition = app.project.activeItem;
if (!composition || !(composition instanceof CompItem)) {
  return alert('Please select a composition first');
}

// Create a Solid Layer with base color of Labels.rgb
var layer = composition.layers.addSolid(
  Labels.rgb / 255,
  'My Layer',
  composition.width,
  composition.height,
  1
);

// Set layers comment to Labels.hex color:
layer.comment = Labels.hex;

// Set layer name to Label.name
myLayer.name = Labels.name;

// Check if layer index matches Labels.index:
var layerIndex = layer.index;
var labelsIndex = Labels.index;
if (layerIndex === labelsIndex) {
  alert('Layer index of ' layerIndex + ' matches the label index of ' + labelsIndex);
} else {
  alert('Layer index of ' + layerIndex + ' does not match the label index of ' + labelsIndex);
}
```

---

## How to use

1. Download the snippet file from the list above and unzip it.
2. In the [Labels](/interface#main-ui) interface click on the **Settings (S)** button to open up the [Settings](/interface#settings) window.
3. In the [Settings](/interface#settings) window click the **Open snippet editor** button to open the [snippet editor](/interface#snippet-editor) window.
   1. Assing the keyboard key to be pressed to launch the snippet, for example *z*.
   2. Set the **path to script file** by clicking on **...** and selecting the snippet file that has extension *.js*.
   3. Click **save** to confirm.
4. Back in AE hold down the *key* you have assigned in previous step (i.e. *z*) and click on any label swatch in the [labels](/interface#main-ui) interface - this should launch the snippet that has been assigned to key *z*.
