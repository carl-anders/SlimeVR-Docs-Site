---
layout: page
nav_order: 5
parent: SlimeVR setup
---

# Setting up reset bindings
{:.no_toc}

Reset bindings are one of the most essential features to set up for an enhanced experience.
Allowing you to reset in a matter of seconds or less.
In this guide we'll show you how to set them up.

# Table of contents
{:.no_toc}

* TOC
{:toc}

# What is a reset?

A reset is the action of resetting the slimeVR skeleton model to a default pose.
This is needed to mitigate any drift you may experience overtime.
You have the option of reset or fast reset, whichever you use depends on your situation.
Reset will do a full reset where by you have to stand straight, look forward and reset (with standard 6 point tracking it is not required to t-pose).
A fast reset is used to clear drift, and only resets the axis along which drift occurs.
Now that you know what a reset is, let's set up a fast way to trigger these resets!

# Which reset type to use?
The type of reset is completely dependent on your position or circumstances.

## Reset:
A standard reset is used to completely restore your skeleton model to it's default pose.
This is done by standing up straight, looking forward and performing the reset.
This can only works as intended when standing up.

## Fast Reset
A fast reset only resets/corrects for any potential drift on one axis.
Whilst less accurate this allows you to reset whilst sitting/laying down.
It is recommended to straighten your limbs and look forward whilst doing this for optimal results.
This method makes it possible to not have to get up every time you have to reset.


# Feeder app

To set up reset bindings for SlimeVR you can use the [feeder-app](https://github.com/SlimeVR/SlimeVR-Feeder-App), which is included by default in the SlimeVR-Installer version 0.1.5 and up.
If you are running an outdated version of SlimeVR without the feeder app, you can download the [latest version](https://github.com/SlimeVR/SlimeVR-Installer/releases/latest/download/slimevr_web_installer.exe) and install it.
This makes setting up reset bindings a lot easier.
You can use the included video for a visual guide on how to set up the reset bindings.

## Setup
{:.no_toc}

To set up reset bindings using the feeder-app you do the following:

1. Head over to your SteamVR settings (make sure "Advanced Settings" is enabled).
2. Go to Controllers > "Show old binding UI" > "show more applications".
3. Scroll down and select "SlimeVR-Feeder-App".
4. Pick a button on your controller to use for the reset binding.
5. Now you can set up a key combination or behavior to perform: "Reset" or "Fast Reset". (see video for clarification)

And you're done!
You're now all set up to have blazingly fast resets.
*Fastest reset in the west*.

You can set this up in whatever way works for you!
Most people opt for either a double tap, long press or button combinations/chords.
This choice is totally up to you.

<div class="video-container">
<iframe width="100%" height="auto" src="https://www.youtube.com/embed/iTOyCOT44d0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

# OVR Advanced Settings

The SlimeVR Server has the following default key bindings:

- `CTRL+ALT+SHIFT+U` for Quick reset.
- `CTRL+ALT+SHIFT+Y` for Reset.

These keybindings can be configured by editing the following line of the `vrconfig.yml` file:

```yaml
keybindings: {reset: CTRL+ALT+SHIFT+Y, quickReset: CTRL+ALT+SHIFT+U}
```

If you want to be able to bind these to your controller, you will need an additional application such as [OVR Advanced Settings](https://store.steampowered.com/app/1009850/OVR_Advanced_Settings/).

### OVR Advanced Settings bindings
{:.no_toc}

Make sure OVR Advanced Settings is closed before following these steps or you will encounter problems.

1. In the Windows Explorer window, enter `%appdata%\AdvancedSettings-Team\OVR Advanced Settings.ini` in **Address bar** and press Enter. Notepad with the `OVR Advanced Settings.ini` file contents should open.
1. Find the `keyboardOne` and `keyboardTwo` lines and replace them with the following lines:

   ```ini
   keyboardOne=^*>y ; CTRL+ALT+SHIFT+Y - Reset
   keyboardTwo=^*>u ; CTRL+ALT+SHIFT+U - Quick reset
   ```

   > **Note:** If you changed default SlimeVR Server key bindings, refer to [Keyboard Input Guide](https://github.com/OpenVR-Advanced-Settings/OpenVR-AdvancedSettings/blob/master/docs/keyboard_input_guide.md).

1. In SteamVR Dashboard, open OVR Advanced Settings and select **Bindings**. If you don't see the icon for OVR Advanced Settings on your dashboard, try running OVR Advanced Settings from your Steam library and check if the icon appeared on your dashboard.
1. In the opened window, select the **Misc** tab.
1. Double-click the plus sign near the desired button name to add a binding.
1. In the opened dialog window, select **BUTTON**.
1. Click **None** near the desired button action. To see more button actions, click **Show more**.
1. In the opened **Boolean Actions** window, select **Keyboard Shortcut One**.
1. Repeat previous two steps for **Keyboard Shortcut Two**.

<div class="video-container">
<iframe width="100%" height="auto" src="https://www.youtube.com/embed/KuCjmHBpH7E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Notes
{:.no_toc}

- If you reset your playspace (for example long pressing Oculus button on Quest), you will need to do a [tracker reset](#reset-trackers).
- OpenVR Advanced Settings' keybinds may not work well in certain languages. If this is the case for you, start SteamVR with your system's language set to English.
- SlimeVR Server uses [Java 11](https://adoptium.net/releases.html?variant=openjdk11&jvmVariant=hotspot).
- If you need the SlimeVR Steam driver you can find it [here](https://github.com/SlimeVR/SlimeVR-OpenVR-Driver/releases/latest/download/slimevr-openvr-driver-win64.zip).

*Created by Eiren, edited by adigyran#1121, CalliePepper#0666, Smeltie#1999 and Emojikage#3095, styled by CalliePepper#0666. Videos created by ZRock35#9574*
