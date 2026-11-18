# Kane & Lynch 2 VR

**[Download 0.6.41](https://github.com/andreystashev/kane-lynch2-vr-showcase/releases/tag/v0.6.41)** · [Installation](INSTALLATION.md) · [Controls](CONTROLS.md) · [Known issues](KNOWN-ISSUES.md)

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
- Physical magazine / cylinder reloads and slides / charging handles for supported weapons.
- Physical peeking and hold-B vaulting without the cover-entry sequence.
- Movement within the moving helicopter passenger cabin.
- Two-handed support and a two-second grip hold for eligible left-hand transfers.
- Controller navigation for menus and a VR height/body calibration.
- Game audio routing to the selected headset.

The standard weapon crosshair and experimental VR cutscenes are off by default.
You can enable them in **Modifiers**. Existing choices are kept when updating.

## What's new in 0.6.41

- Tap **A** with the movement stick centred to reload. Hold **A** while moving
  to sprint. Releasing **A** early during movement leaves the magazine in place.
- Subtitles, speaker names and icons move together toward the centre. The
  original crosshair keeps its proportions, and the laser tracks more consistently.
- The settings window has fewer switches. Helicopter escape prompts show VR buttons.
- Improved throwing, magazine handling, camera settling and getting up near cover.
- Both native eye views render from one game update in supported scenes. The
  renderer reuses more work between eyes and across layers of the HUD.

**Rare Steam crashes and stutter remain possible.** See the
[release notes](RELEASE-NOTES.md) and [known issues](KNOWN-ISSUES.md).

## Install and play

1. Run the original game through Steam at least once.
2. Download `KaneLynch2VR-0.6.41-Setup.exe` from the
   [release page](https://github.com/andreystashev/kane-lynch2-vr-showcase/releases/tag/v0.6.41).
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
| Left stick | Move, including inside the helicopter passenger cabin. |
| Left stick click | Switch walking / ordinary running while standing. |
| Right stick | Turn. |
| Hold right stick click | Calibrate VR height and body position. |
| Trigger on the weapon hand | Fire. |
| A | Tap with the movement stick centred to reload. Hold while moving to sprint. |
| B | Tap to crouch / stand or get up when wounded; hold near a low obstacle to vault. |
| X | Interact, pick up, or use a contextual action. |
| Y | Tap to change weapon. Hold to show the HUD. |
| Grip | Support, magazine or charging handle; hold receiving grip 2s with hands together to transfer. |
| Menu | Pause. |

**Vaulting:** face an eligible low obstacle with the headset, approach and
hold **B** for about 0.35 seconds. Lean physically to peek around obstacles.

For physical reloading, centre the movement stick and tap **A**. Grip near the shoulder or hip with a free hand,
bring the spare to the well and release. Grip and pull the slide / charging handle
if needed. **Physical magazine reload (experimental)** and **Recover ammo from
ejected magazines** are in Modifiers. Physical reload starts enabled on fresh
installs; explicit existing choices are preserved. Ejected magazines disappear
and cannot be collected. See [Controls](CONTROLS.md) for the full sequence.

Eligible one-handed guns transfer with a roughly two-second receiving-grip hold
with hands together. This moves the same gun; two independent guns at once are
not supported.

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

- **Crashes and freezes:** random failures remain during mission loading and
  sometimes gameplay. A `Rendering_Setup` error can leave the headset image frozen.
  The game's 32-bit memory limits also remain a constraint.
- **Stereo timing:** supported gameplay scenes render both eyes in one game update.
  Other scenes can use sequential eye updates or a flat display.
- **Missing textures and objects:** some scenery can disappear and reappear at
  particular distances, and texture detail can change unexpectedly.
- **Movement:** direct vaulting and physical peeking adapt a third-person game;
  collision, scripted interactions and some poses still have limitations.
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
to reproduce the problem.

For intermittent problems, enable **Modifiers → Record diagnostic logs** in
the settings window, save, and restart the game. Logging is off on a fresh
installation. After the problem occurs and you have closed the game, run
`Collect-KL2-Diagnostics.cmd` from the mod folder. It creates a ZIP in
`diagnostics/` from retained session logs. No video is needed and nothing is
sent automatically. See the [diagnostics guide](INSTALLATION.md#diagnostic-logs)
for details. Review the archive before sharing it publicly.

## Credits

Created by [andreystashev](https://github.com/andreystashev).
Bundled components retain their own licenses; see
[third-party notices](THIRD-PARTY-NOTICES.md).

Kane & Lynch 2 and its game assets belong to their respective owners. This is
an independent community mod, not an official IO Interactive or publisher release.

This repository hosts downloads, player documentation and issue reports.
