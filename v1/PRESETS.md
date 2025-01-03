# The Presets (v1)

> This is an archived version of the v1 preset catalog. In v2, Quick Spotlight changed so that when Spotlight would only appear when Command was pressed alone, and when used with another key would translate to Control + Key. This removed the press-for-siri functionality I never used, and fixes the inability to use Control in terminal environments and with some niche shortcuts

### Control to Command > *ctrl-to-cmd-v1.json*
This version excluded MacOS's Terminal because most shortcuts in Terminal to allow the use of Control in shortcuts. This was updated in v2 to simply use Command for Control in the quick spotlight preset.

### Quick Spotlight / Hold for Siri > *macos-quick-spotlight-v1.json* 
This version would fire dictation if the Command key was held.
> This works best if you enable *Always Show Siri Captions* in the **Siri Responses** settings of your Mac.

# Deprecated Presets

### [DEPRECATED] Quick Arc Tab / Hold to Dictate > *quick-arc-tab.json*
This file maps a tap on the Command key to a New Tab action, but exclusively in Arc (My browser of choice).
> The browser can be modified by editing the `conditions.bundle_identifiers` property to detect a different browser's package name.

This carries over the hold action from Quick Spotlight, triggering text dictation. Releasing hold stops dictation.
> To use this, you should have dictation mapped to the Microphone key in the settings of your Mac.

### [DEPRECATED] VSCode Terminal Ctrl + C > *vscode-terminal-kill.json*
This file mapped the Command + C key to the Control + C key combination ONLY IN VSCODE, which is used by some terminal processes as a stop signal. 

In order for this to not wipe out copy commands, I had to go through VSCode's keyboard shortchuts and **add** Ctrl + C to each command that was using Cmd + C. This was inefficient and would not work on a fresh system without in-depth reconfiguration. The v2 Quick Spotlight change also removes the need for this preset.