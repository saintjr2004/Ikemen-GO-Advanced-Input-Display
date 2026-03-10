# Advanced Input Display Module for IKEMEN GO

This is a module for the IKEMEN GO engine that displays your inputs in training mode
in a way similar to that of commercial fighting games, displaying both your inputs and
the time (in frames) you had held that particular combination for.

## Installation

Extract the `jayinputdisplay` folder directly into the folder you wish to store it in.
It's recommended you place it in `external/mods` since it is a module.

You will need to make edits to your current IKEMEN config.ini file to "enable" the module.

Under `[Common]`, add `jayinputdisplay.zss` to your `States` files and `jayinputdisplay.def` to your `Fx` files.

Example with the files stored in `external/mods`:

```
[Common]
...
States  = data/functions.zss, data/action.zss, data/dizzy.zss, data/guardbreak.zss, data/score.zss, data/system.zss, data/tag.zss, data/training.zss, external/mods/jayinputdisplay/jayinputdisplay.zss
Fx      = data/gofx/gofx.def, external/mods/jayinputdisplay/jayinputdisplay.def
```

## Configuration

Within `jayinputdisplay.zss`, you have several configuration options to tweak the display and behavior of the buttons and timer text.

```
#============
# CONFIG
#============

map(jayinput_enabled) 			:= 1;			# Enable input display (0 = off, 1 = on)
map(jayinput_xPos)				:= 20;			# X pos for the input display to start on
map(jayinput_yPos)				:= 85;			# Y pos for the input display to start on
map(jayinput_rowSpacing) 		:= 12;			# Spacing between input lines
map(jayinput_columnSpacing) 	:= 12;			# Spacing between input combinations
map(jayinput_btnScale) 			:= 0.5;			# Scale for buttons
map(jayinput_btnCount)			:= 11;			# Amount of rows to display (up to 16 items)
map(jayinput_sprPriority)		:= 512;			# SprPriority parameter value for the buttons
map(jayinput_onTop)				:= 1;			# Ontop parameter value for the buttons
map(jayinput_layer)				:= 1;			# Layer parameter value for the buttons

map(jayinput_textEnable)		:= 1;			# Enable timer text (0 = off, 1 = on)
map(jayinput_textFont) 			:= 3;			# Font used for the timer text (Uses fight.def fonts by default)
map(jayinput_textBank) 			:= 0;			# Color bank used for the timer text
map(jayinput_textLayer)			:= 2;			# Layer used for the timer text
map(jayinput_textXPos)			:= 200;			# X pos for timer text
map(jayinput_textP2Off)			:= 875;			# X offset for P2 side
map(jayinput_textYPos)			:= 260;			# Y pos for timer text
map(jayinput_textSpacing)		:= 36;			# Line spacing for timer text
map(jayinput_textScale) 		:= 0.75;		# Scale used for the timer text
map(jayinput_textCap)			:= 999;			# Max time displayed for a held input

map(jayinput_enableLP)			:= 1;			# Allow detection of LP/X (0 = no, 1 = yes)
map(jayinput_enableMP)			:= 1;			# Allow detection of MP/Y (0 = no, 1 = yes)
map(jayinput_enableHP)			:= 1;			# Allow detection of HP/Z (0 = no, 1 = yes)
map(jayinput_enableLK)			:= 1;			# Allow detection of LK/A (0 = no, 1 = yes)
map(jayinput_enableMK)			:= 1;			# Allow detection of MK/B (0 = no, 1 = yes)
map(jayinput_enableHK)			:= 1;			# Allow detection of HK/C (0 = no, 1 = yes)
map(jayinput_enableD)			:= 1;			# Allow detection of D (0 = no, 1 = yes)
map(jayinput_enableW)			:= 1;			# Allow detection of W (0 = no, 1 = yes)
map(jayinput_enableS)			:= 1;			# Allow detection of Start (0 = no, 1 = yes)
```

You can edit `jayinputdisplay.sff` and `jayinputdisplay.air` directly to further tweak the appearance of the inputs.
