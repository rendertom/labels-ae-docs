# Known issues

All notable issues will be listed here.

---

## Labels do not update in AE

Sometimes After Effects does not redraw the interface once you install or switch to a new labels theme. To fix this, simply mouse-click anywhere in the AE interface (timeline, preferably) to force AE to redraw the interface.

## Cannot color Layers and Items

Ensure that the [Settings > Set color](/interface#settings) option is enabled, and verify whether any modifier keys are assigned to it. By default, no modifier keys should be assigned to this action.

## Cannot color Keyframes

Requires AE v22.6 or later.

To color keyframes, hold the `CMD` key (on Mac) or the `CTRL` key (on Windows) while clicking on a label. If this method does not work, ensure that the [Settings > Target keyframes](/interface#settings) option is enabled. Additionally, verify which keyboard modifier key is assigned for this action and use that key instead.

## It just does not work

In some rare cases, when Labels refuse to work, it's recommended to delete the preferences files and start over. To do this, follow the steps below:

  1. In After Effects, open the **Settings** window and navigate to the **Startup & Repair** section.
  2. Click the **Reveal Preferences in Finder** button. This will open a new folder where the After Effects preference files are stored.
  3. Close After Effects.
  4. Locate and delete the following two files. *NOTE: These files contain configuration options for your other installed scripts as well as some internal After Effects preferences, so back these files up if you need to revert this step.*
     - Adobe After Effects [version] Prefs-indep-general.txt
     - Adobe After Effects [version] Prefs.txt
  5. Launch After Effects and Labels.
