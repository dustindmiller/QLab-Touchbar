# QLab-Touchbar
Touchbar Preset for BetterTouchTool

Hello there!
The process is deceptively simple when looked at in its broad sense, but I'm available for any and all questions you may have while trying to get things up and running.

For more information on the look & feel of the Touchbar, jump over to my [blog post](https://www.dustindmiller.design/post/qlab-4-now-with-touch-bar).

## BetterTouchTool Import

First, jump online and download [BetterTouchTool](https://folivora.ai/). Purchasing the full version of the app is always best when utilizing it's services to the extent this preset does, but the free version should do for our needs.

Open up BTT and, if it isn't there already, navigate to the Touch Bar settings option on the drop down in the top section of the app:

![BTT Touchbar Tab](https://cdn.discordapp.com/attachments/817192452997251072/817192566289858590/0.png)

Once here, click on the "Preset: Master"  drop down and select "Import"

![BTT Import Preset](https://cdn.discordapp.com/attachments/817192452997251072/817192600041816094/0.png)

Navigate to the downloaded BTT preset file and follow the prompts.

NOTE: If it asks you to overwrite, please take caution if you have a custom Touch Bar preset for QLab already, as this will remove it.

## macOS System Keyboard Shortcuts

Once this is all set, open up System Preferences for your Mac and open up Keyboard > Shortcuts. Add three new Shortcuts for "Save As Template," "Bundle Workspace," & "Record cue sequence...":

![macOS Custom Keyboard Shortcuts](https://cdn.discordapp.com/attachments/817192452997251072/817192628952367144/0.png)

If you are unsure of how to do this, here is a quick how-to guide: https://support.apple.com/guide/mac-help/create-keyboard-shortcuts-for-apps-mchlp2271/mac

## QLab Workspace Settings

Now the fun part...

I have network patches set by default in a template file:

![QLab Network Patch](https://cdn.discordapp.com/attachments/817192452997251072/817192663891050566/0.png)

You can use whatever Name, Type, Network, Destination, Port or Passcode for all of these, but the device type (QLab Machine, Eos/Hog & X32) must be Patched in this order in your workspace or some, if not all of the custom script commands will not work.

## Custom Scripts

The custom scripts I have have also can sometimes be a challenge to get to work correct;y, so please review the following notes before utilizing them:

### Edit/Show Mode Toggle

![Show/Edit Mode Button](https://cdn.discordapp.com/attachments/817192452997251072/817192702675910656/0.png)

This button "toggles" Edit & Show mode.
Essentially it cleans up the "Main" Touch Bar from this:

![Edit Mode Touchbar](https://cdn.discordapp.com/attachments/817192452997251072/817192729351290890/0.png)

...to this:

![Show Mode Touchbar](https://cdn.discordapp.com/attachments/817192452997251072/817192757465972786/0.png)

That being said, if you navigate away from QLab, you will have to hit the toggle again to display the "Show Mode" Touch Bar, but your workspace will remain in Show Mode regardless.

### Legacy Continue Mode Toggle

![Auto-Continue Mode Button](https://cdn.discordapp.com/attachments/817192452997251072/817192784044884019/0.png)

This is a script command that cycles the Continue mode of the selected cue (or cues) to the "next" continue mode in the list.
I made this after Figure 53 implemented the drop-down menu approach.

### Fade Cue Set
PREP: Number and name selected cue before running this cue.

ACTION: Select cue and run this cue to create a Group Cue with the Audio/Mic/Video/Camera/Text Cue and a Fade In cue, followed by a Fade Out cue.

NOTE: Blank text will select defaults for those parameters.


### LX

PREP: Set Network Patch #4 for Eos or Hog System before running script.

ACTION: Select cue in main Cue List and run this cue to create a new Network Cue to trigger a cue on a Eos or Hog Lighting System.

NOTES: Eos Win 7+ and Hog 4+ Consoles ONLY.


### SX

PREP: Set Network Patch #5 for X32 System before running script.

ACTION: Select cue in main Cue List and run this cue to create a new Network Cue to set Mute On or Off for any Channel or Bus on an X32 System.


### QX

PREP: Set Network Patches #1–3 for QLab Systems before running cue.

ACTION: Select cue(s) to build new cuelist with Network cues to Start cue(s) in different workspace/list.

NOTE: Ensure all selected cues have cue numbers or letters (No spaces) & that all other workspace cue numbers do not conflict
