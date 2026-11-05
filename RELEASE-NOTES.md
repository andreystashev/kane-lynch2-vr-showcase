# Kane & Lynch 2 VR 0.6.25

The first public release of my VR mod for **Kane & Lynch 2: Dog Days**.

## Included

- First-person stereo VR with head tracking, tracked hands and physical aiming.
- Quest Link / Air Link, Virtual Desktop / VDXR, SteamVR / Steam Link and OpenXR
  connection profiles.
- A settings launcher with Original, DXVK and D3D9On12 renderers.
- A red laser, hit feedback, hand-based ammo and action information, and optional
  controller hints.
- Support grips and transfer of eligible one-handed guns to the left hand.
- Controller menu navigation and VR height/body calibration.
- Headset audio routing and improved image stability in OpenXR connections.

## Before playing

This is an early release for the **Windows Steam version, single player**.
Co-op and multiplayer have not been run or tested; their operation is not
guaranteed. Other game editions are unverified.

Crashes remain possible because of the game's memory limits and runtime checks.
They happen most often during mission loading, but can also occur during gameplay.
Some textures or objects may disappear at particular distances. Cover movement,
grips and scripted interactions still need work. Two separate guns at once and
automatic VR scope zoom are not supported.

**For the required vault in the first mission:** hold **B** to enter cover,
release it, then **hold B again while moving the left stick** toward the obstacle.
Tap B to leave cover normally.

## Download and update

Use `KaneLynch2VR-0.6.25-Setup.exe`, or extract the Portable ZIP into its own
folder. Close the game and settings window before updating. Settings and saves
are kept. The release contains no video recorder or developer tools.

Set graphics quality and resolution in the original game's menu, then restart.
D3D9On12 is the default renderer; Original and DXVK are alternatives. Performance
varies by scene, hardware and headset settings.

See [installation](INSTALLATION.md), [controls](CONTROLS.md) and
[known issues](KNOWN-ISSUES.md) for the full guide.

Created by [andreystashev](https://github.com/andreystashev).

