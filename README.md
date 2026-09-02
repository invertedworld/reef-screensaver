# Reef

A macOS screensaver: an endless coral reef, generated as you watch it.

The camera flies itself — long banked turns over the seabed, a rise into open
water, a slow pass by whatever school happens to be worth looking at. No two
sessions are the same reef.

<br>

## Install

Download **`Reef-1.0.pkg`** from
[Releases](https://github.com/invertedworld/reef-screensaver/releases/latest),
double-click it, and follow the installer.

Then open **System Settings → Screen Saver** and choose **Reef**.

The installer is signed with a Developer ID and notarized by Apple, so it opens
without the "unidentified developer" warning.

<br>

## Requirements

|                |                                        |
| -------------- | -------------------------------------- |
| **macOS**      | 13 Ventura or later                    |
| **Mac**        | Universal — Apple silicon and Intel     |
| **Graphics**   | Any GPU that runs WebGL 2               |

The reef is rendered live rather than played back, so it uses the GPU while it
is on screen. On a laptop running on battery you may prefer a shorter
"Start Screen Saver when inactive" setting.

<br>

## What it draws

Everything on screen is computed rather than recorded.

- **The seabed** is a procedural field — reef flats, sand channels, dunes and
  bommies — streamed in around the camera as it travels.
- **The caustics** come out of the optics rather than a texture loop: sunlight
  refracting through the swell is a map from the surface to the seabed, and the
  bright filigree is exactly where that map folds.
- **Snell's window** is the real thing. Looking up, the entire sky is
  compressed into a 48-degree cone overhead, and outside it the surface is a
  mirror — drawn by the Fresnel equations, so the rim of the window is physics
  rather than a threshold.
- **Thirty species of fish**, schooling, feeding, hunting and scattering; crabs
  walking the sand sideways; moray eels gaping from the reef wall.
- **Colour** falls off the way it really does underwater — red is gone within
  the first ten metres — with the same white balance a diver's eye or an
  underwater camera applies to get it back.

<br>

## Uninstall

```
sudo rm -rf "/Library/Screen Savers/ReefSaver.saver"
```

<br>

---

This repository hosts the installer only. Source is not included.
