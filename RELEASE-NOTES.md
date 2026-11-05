# Kane & Lynch 2 VR 0.6.30

This update improves Steam executable compatibility, cover selection, throwable
aiming and recovery from an audio memory allocation failure.

## Changes

- Recognizes an additional Steam executable variant that earlier installers
  rejected. Setup and the launcher now use the same executable checks.
- Cover selection follows headset facing, including while standing still.
- Canisters and cylinders follow the current aiming direction when thrown.
- Improves recovery from audio-buffer allocation failures during gameplay.
- Improves weapon grip initialization when a mission starts or the character
  rig changes.
- Includes the earlier SteamVR startup and headset-audio fixes.

## Updating

Close the game and mod settings window, then install
`KaneLynch2VR-0.6.30-Setup.exe` over your existing mod installation. Your mod
settings and saved games are kept. Use the complete package when updating.

The Portable ZIP is available as an alternative. Extract it into its own folder,
connect the headset, open **Kane & Lynch 2 VR Settings** and choose **Save & play**.

## Before playing

This remains an early release for the **Windows Steam version, single player**.
Co-op and multiplayer have not been run or tested; their operation is not
guaranteed. Compatibility with other game editions can vary.

The game's 32-bit memory limits still apply. Crashes, stutter, missing scenery
and changes in texture detail can still occur. Cover, grips, reloads and some
scripted interactions can feel awkward. Two independent guns at once and
automatic VR scope zoom are not supported.

For the required vault in the first mission: hold **B** to enter cover, release
it, then **hold B again while moving the left stick** toward the obstacle.
Tap B to leave cover normally.

See [installation and renderers](INSTALLATION.md), [controls](CONTROLS.md) and
[known issues](KNOWN-ISSUES.md) for the full guide.

Created by [andreystashev](https://github.com/andreystashev).
