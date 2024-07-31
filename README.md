# Karabiner-Elements Presets
As a long-time Windows user, entering MacOS was really jarring. I was used to smacking the Win key and typing out whatever I wanted to search and getting quick web results. That's why I started mapping my command key to Spotlight search. These files are advanced configurations I've made since then to improve my experience, mostly focusing on the power of the Command key.

# Installation
> Before choosing your presets, install "Control to Command" first.

After installing Karabiner-Elements to your MacOS system:
- Navigate to the **Complex Modifications** tab in the Karabiner-Elements App
- Click the *Add Your Own Rule* button
- Replace the entire contents of the text box with the contents of one of these files
- Click the Save button

# The Presets

### Control to Command > *ctrl-to-cmd.json*
This file maps any press of the Control key to the Command key, as most shortcuts in MacOS primarily use Command. This allows the rest of the Command actions in this repo to work.

This excludes MacOS's Terminal because most shortcuts in Terminal use Control by default.

### VSCode Terminal Ctrl + C > *vscode-terminal-kill.json*
This file maps the Command + C key to the Control + C key combination ONLY IN VSCODE, which is used by some terminal processes as a stop signal. 
> In order for this to not wipe out copy commands, I went through VSCode's keyboard shortchuts and **added** Ctrl + C to each command that was using Cmd + C.

### Pause to Lock Screen > *pause-locks-screen.json*
This file maps the Pause key to the Command + Control + Q key combination, which locks the screen. This is a replacement for my brain-trained Win + L to lock command.

### Print Screen to Screenshot > *print-screen-capture.json*
This file maps the Print Screen key to the Command + Shift + 5 key combination, which opens the screenshot app, similar to how Windows will launch Snipping Tool.

### Quick Spotlight / Hold for Siri > *macos-quick-spotlight.json* 
This file maps a tap on the Command key to open Spotlight Search. This follows the original goal I had.
It also listens for a short hold on the Command key, and triggers Siri if so. When a hold is released, Siri is either cancelled or executes what you said.
> This works best if you enable *Always Show Siri Captions* in the **Siri Responses** settings of your Mac.

### Quick Arc Tab / Hold to Dictate > *quick-arc-tab.json*
This file maps a tap on the Command key to a New Tab action, but exclusively in Arc (My browser of choice).
> The browser can be modified by editing the `conditions.bundle_identifiers` property to detect a different browser's package name.

This carries over the hold action from Quick Spotlight, triggering text dictation. Releasing hold stops dictation.
> To use this, you should have dictation mapped to the Microphone key in the settings of your Mac.
