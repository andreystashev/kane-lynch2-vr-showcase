# Kane & Lynch 2 VR

**[Download 0.6.25](https://github.com/andreystashev/kane-lynch2-vr-showcase/releases/tag/v0.6.25)** · [Installation](INSTALLATION.md) · [Controls](CONTROLS.md) · [Known issues](KNOWN-ISSUES.md)

An unofficial first-person VR mod for **Kane & Lynch 2: Dog Days** on Windows,
created by [andreystashev](https://github.com/andreystashev).

Play the single-player campaign with stereoscopic rendering, head tracking,
tracked hands and physical weapon aiming. This is an early release: crashes,
missing surfaces and awkward interactions are still possible.

You need your own copy of the game. The mod was tested with the
**Windows Steam version** in single player. Co-op and multiplayer have **not been run or tested**;
their operation is not guaranteed. Other game editions are also unverified.

## Features

- First-person VR view with head tracking and controller-driven hands and weapons.
- Quest Link / Air Link, Virtual Desktop / VDXR, SteamVR / Steam Link and OpenXR
  connection profiles in the settings window.
- Original Direct3D 9, DXVK and D3D9On12 renderers.
- A red aiming laser, hit feedback, and ammo and action information beside your hands.
- Two-handed weapon support and left-hand transfer for eligible one-handed guns.
- Controller navigation for menus and a VR height/body calibration.
- Game audio routing to the selected headset.

The standard weapon crosshair is off by default and can be enabled in settings.
The other gameplay modifiers start enabled. Your choices are kept when updating.

## Install and play

1. Run the original game through Steam at least once.
2. Download `KaneLynch2VR-0.6.25-Setup.exe` from the
   [release page](https://github.com/andreystashev/kane-lynch2-vr-showcase/releases/tag/v0.6.25).
3. Install the mod in its own folder, outside the game folder.
4. Connect the headset, then open **Kane & Lynch 2 VR Settings**.
5. Check the detected game, select your headset connection and renderer, and
   choose **Save & play**.
6. Stand naturally and hold the **right stick click for about 0.65 seconds**
   to calibrate VR height and body position.

The regular **Kane & Lynch 2 VR** shortcut starts the game with your saved
settings. A portable ZIP is available as an alternative to installation.
See the [installation guide](INSTALLATION.md) for connection setup and removal.

## Controls

The guide uses the A/B/X/Y layout found on Quest/Touch-style controllers.
Other controllers may need different runtime bindings.

| Control | Main action |
| --- | --- |
| Left stick | Move; peek while in cover. |
| Left stick click | Switch walking / ordinary running while standing. |
| Right stick | Turn. |
| Hold right stick click | Calibrate VR height and body position. |
| Trigger on the weapon hand | Fire. |
| A | Tap to reload; hold while moving to sprint. |
| B | Tap to crouch / stand or leave cover; hold to enter cover. |
| X | Interact, pick up, or use a contextual action. |
| Y | Tap to change weapon; hold for hand hints, ammo and action information. |
| Grip | Support a weapon or transfer an eligible one-handed gun. |
| Menu | Pause. |

**Cover and vaulting matter for progression.** Hold **B** to enter cover, then
release it to stay there. Use the left stick to peek. To move between cover or
vault an obstacle, release B and then **hold B again while moving the left stick
toward the destination**. The first mission has a required obstacle that uses
this sequence. Tap B to leave cover normally.

Pistols, revolvers and eligible SMGs can be moved to the left hand. This transfers
the same gun; **holding and firing two separate guns at once is not supported**.
See the [full controls guide](CONTROLS.md) for grips and human-shield actions.

## Renderers and performance

| Renderer | Use |
| --- | --- |
| **D3D9On12** — default | Runs Direct3D 9 through Direct3D 12 and uses GPU image transfer when available. A starting point on compatible Windows systems and drivers. |
| **DXVK** | Runs Direct3D 9 through Vulkan. An alternative whose performance and compatibility depend on the GPU and driver. |
| **Original** | Uses the game's Direct3D 9 renderer. Useful when comparing compatibility with the other options. |

Original and DXVK can spend more CPU time transferring the VR image than the
D3D9On12 GPU path. The old game engine can also be CPU-limited, so reducing
resolution or graphics quality does not always remove stutter. No renderer is
the fastest on every PC; compare them in the same scene and settings.

Change resolution and graphics quality **inside the game**, then restart it.
Close the game before switching renderers. Headset resolution and refresh rate
are controlled by your PC VR application and also affect performance.

## Current limitations

- **Crashes:** the original game's 32-bit memory limits and runtime checks
  constrain the mod's memory workarounds. Crashes are most likely during mission
  loading, but can also occur in gameplay, especially in long sessions.
- **Missing textures and objects:** some scenery can disappear and reappear at
  particular distances, and texture detail can change unexpectedly.
- **Movement and cover:** the game was designed for third-person play. Cover,
  vaulting and some scripted interactions are still awkward in VR.
- **Hands and animation:** some grips, reloads, body poses and shadows can look
  unnatural. Large physical leaning can move the camera through walls.
- **Weapons:** independent dual wielding and automatic VR sniper-scope zoom are
  not available.
- **Online play:** co-op and multiplayer have not been run or tested and may not work.

Read [known issues and troubleshooting](KNOWN-ISSUES.md) before playing. If a
mission transition crashes, restart the game and try your latest checkpoint.

## Reporting problems

Use [Issues](https://github.com/andreystashev/kane-lynch2-vr-showcase/issues) and
include the mod version, headset connection, renderer, mission and steps needed
to reproduce the problem. Do not post private files or personal information.

## Credits

Created by [andreystashev](https://github.com/andreystashev).
Bundled components retain their own licenses; see
[third-party notices](THIRD-PARTY-NOTICES.md).

Kane & Lynch 2 and its game assets belong to their respective owners. This is
an independent community mod, not an official IO Interactive or publisher release.

This repository hosts downloads, player documentation and issue reports.
