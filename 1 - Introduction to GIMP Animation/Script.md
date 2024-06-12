## Introduction

Hello everybody, Alex here!

In this video, I will show you how to create hand-drawn 2D animation using GIMP, and use these skills to animate a bouncing ball. GIMP is traditionally an image-editing software, but with a bit of tweaking, you can use it to make 2D animations!

The aim of this video is to teach you how GIMP can be used as an animation software and to teach some basics of 2D animation. 

### What can you animate with GIMP?

You can animate anything with GIMP given enough time, effort, and patience! I have personally used GIMP to create animated sprites for my video game Moomoo's Maple Mishap and for the open-source game SuperTux, as well as to create fighting game character animations.

### Why animate with GIMP rather than other software?

#### Pros:
- GIMP is free and open-source. You will always be able to download GIMP for free and own all of the work that you create using the application.

- GIMP is lightweight and is easy to install and uninstall.

#### Cons:
- GIMP was not designed to be an animation software. Other free animation applications like Krita, FireAlpaca, and Blender are far more intuitive and usable than GIMP. To make GIMP behave like a 2D animation software, a number of configurations to it must be made, which are explained here.

- GIMP 2.8 has no built-in support for animation frames. Instead, each layer of your image will be treated as an animation frame. To have layers within animation frames, each animation frame needs to be a layer group.

- GIMP 2.8's default brushes are bad - there exist no simple "pen pressure = size" brush or "pen pressure = size and opacity" brushes by default, so I have created them and have provided them for you to use.

- GIMP 2.8 has an unintuitive user interface. Most of GIMP's keyboard shortcuts are completely different to mainstream art programs like Photoshop, Krita, or Clip Studio Paint. You can re-bind the keyboard shortcuts in the settings to match mainstream art programs, but there is no 'industry standard' keyboard preset you can use to do this automatically, so you have to rebind every shortcut separately.

### How do I make good 2D animations?
I will briefly explain the animation principles of timing, spacing, and squash-and-stretch in this video with the bouncing ball exercise.

If you want to go further, I recommend learning about the 12 principles of animation, which are explained excellently by Alan Becker in his video series: https://www.youtube.com/watch?v=uDqjIdI4bF4

If you want to become a master 2D animator, I recommend reading The Animator's Survival Kit by Richard Williams, or Disney Animation: The Illusion of Life by Frank Thomas and Ollie Johnston. Both are essential guides for becoming a true animator and artist.

You can read The Animator's Survival Kit here: https://archive.org/details/TheAnimatorsSurvivalKitRichardWilliams/

## You will need:
For this tutorial, you will need:

- GIMP 2.8.X (latest version is 2.8.22 as of 12/06/2024)
  - Windows https://download.gimp.org/gimp/v2.8/windows/gimp-2.8.22-setup.exe
  - Mac https://download.gimp.org/gimp/v2.8/osx/gimp-2.8.22-x86_64.dmg
  - Linux https://download.gimp.org/gimp/v2.8/gimp-2.8.8.tar.bz2

- The "Export Layers" GIMP Plugin.
  - https://github.com/kamilburda/gimp-export-layers/releases/

- Two custom GIMP brushes - "Tapering" and "Taper Opacity".
  - _**TODO: ADD BRUSHES HERE**_

- **Optional:** A drawing tablet. Whilst it is possible to draw with your mouse, I recommend getting a drawing tablet to animate on your computer. I use a Wacom Intuos tablet, but there are plenty of other cheap drawing tablets on the market.

## Installation & Configuration Process

A number of steps are needed to configure GIMP as a 2D animation software.

### Display
You'll notice when GIMP 2.8 first launches it looks like a dog's dinner with separate windows regurgitated all over your screen. To fix this, activate 'Single Window Mode' by going to ``Windows > Single Window Mode``.

### Keyboard Shortcuts
For this tutorial, we will be creating some custom keyboard shortcuts in GIMP for functions you will access very often when animating. We will be creating the following keyboard shortcuts:
  - Animation playback (CTRL+P)
  - Resize canvas to selection (CTRL+Shift+C)
  - Resize canvas to fit all layers (CTRL+Shift+V)

To create these shortcuts:
1. Navigate to ``Edit > Keyboard Shortcuts``.
2. Tick "save keyboard shortcuts on exit". This will ensure the changes we make are saved the next time we open GIMP.
3. Search for "playback". You will find the "Playback" action. Click on the "Disabled" text on the shortcut tab to enter a new shortcut for the action. Press CTRL+P on your keyboard to assign the shortcut.
4. Next, search for "canvas" and repeat the steps to assign the shortcuts for Fit Canvas to Layers and Fit Canvas to Selection.

### Brushes
We will be needing to add the following custom brushes to GIMP:
  - Tapering (pen pressure = size)
  - Taper Opacity (pen pressure = size and opacity)

To do this, follow these steps:
1. Navigate to ``Edit > Preferences``.
2. In the Preferences menu, navigate to ``Folders > Dynamics``. You will see the folder path where GIMP stores your Brush Dynamics.
3. Navigate to this folder in your File Explorer.
4. Place the custom brushes into the folder.
5. Keep the preferences menu open for our next step:

### Plug-ins
We also need to install the "Export Layers" plug-in for GIMP so that we can export each frame of our animation as a separate image. To do this, open the preferences menu and follow these steps:

  - In the Preferences menu, navigate to ``Folders > Plug-ins``. You will see GIMP's Plug-in folder path.
  - Navigate to this folder in your File Explorer.
  - Open a separate File Explorer window and open the Export Layers plug-in ZIP file.
  - Copy the "export_layers.py" file and "export_layers" folder into GIMP's plug-in folder.

### Drawing Tablet Set Up (Optional)
- Install the relevant drivers for your drawing tablet. If you are on Windows, ensure Windows Ink Workspace is disabled.
- Close GIMP. Plug in your drawing tablet, then open GIMP again.
GIMP will not recognise your drawing tablet if you plug it in after GIMP starts, so always plug in your tablet before launching GIMP. Frustrating, I know.

- Navigate to Edit > Input Devices. You should see your drawing tablet listed there.
- Set the mode of your tablet to "Screen".
- Select "Save" to confirm your choice.

## Animation Method
With GIMP configured, we can now start animating our bouncing ball!

1. Create new document in GIMP.

2. Optional: Create reference layers to plan out your animation.
For reference layers, adding the suffix ``(1ms)`` to their names to make them not appear during animation playback.

3. Create a layer group for each frame of animation.
Each group should have a background layer as the bottom layer. If you make the background layers partially transparent (e.g., 75% opacity), it will allow you to see previous animation frames.

4. Animate a rough draft of your animation. Use the playback (CTRL+P) feature to preview your animation as you create it. If you need to zoom in on the preview, use Magnifier.

5. Save a copy of your work. Draw the linework for your animation on a separate layer using the Tapering brush. Once completed, hide the sketch layers.

6. Save a copy of your work. Add flat colour to your animation by creating a new base colour layer beneath the linework and drawing the colour using either selection tools or a Tapering brush.

7. Save a copy of your work. Add lighting to your animation by creating a new lighting layer on top of the base colour. Right-click the flat colour layer and select "Alpha to Selection". This will allow you to only draw within the painted areas of the flat colour layer. Now, draw in the *lighting* layer (NOT the base colour layer) with a Pressure Opacity brush to create smooth lighting.

## Exporting your Animation

1. Save a copy of your work.
2. Hide the background colour for each layer of your animation.
3. Delete all reference layers.
4. Use the export layers plug-in to export each layer of your animation as a frame.
5. Alternatively, you can export your animation as a .GIF, but be warned, this will reduce the quality of your animation because GIF files can only contain 256 colours and cannot contain semi-transparent pixels.

## FAQ / Troubleshooting

#### GIMP isn't detecting my drawing tablet
- Ensure you plug in your drawing tablet **before** you launch GIMP 2.8, otherwise it won't recognise it. Frustrating, I know.
- Ensure you have the correct drivers installed.
- Ensure your drawing tablet is activated on GIMP by navigating to ``Edit > Input Devices`` and setting your tablet's mode to "Screen".
- If you are using Windows, ensure that Windows Ink is disabled.
  - This can be disabled on Wacom drawing tablets by opening the "Wacom Tablet Properties" application, navigating to "Mapping", and unchecking the "Use Windows Ink" checkbox.
#### GIMP is taking forever to start up
- This is a known issue, sometimes GIMP will take forever to launch because its "font cache" becomes corrupted. To fix this, you will need to delete GIMP's font cache files, which will force GIMP to create a new, uncorrupted font cache. This video explains how: https://www.youtube.com/watch?v=iiCdCS1CFIc
#### I can't draw on the canvas
- Ensure you are using the Brush tool.
- Ensure the colour you have selected is not same as the background colour.
- Ensure your brush opacity is 100%.
- Ensure your brush size is greater than 0.
- Ensure you have a layer selected, and not a layer group. You can't draw on layer groups.
- Deselect your current selection using the shortcut CTRL+Shift+A.
#### Why the hell would you bother with this?
- You can always use paper or other animation software like FireAlpaca, Blender, Krita, etc. GIMP is not perfect or even ideal, but it is free and fast if you get to know it.