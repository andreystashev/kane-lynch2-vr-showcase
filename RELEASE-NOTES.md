# Kane & Lynch 2 VR 0.6.31

## Steam executable compatibility

Different Steam installations can have different full-file executable hashes.
The installer, launcher and mod now recognize compatible Steam build 3684 files
from the game code, PE layout and native data used by the mod. Previously unseen
files also require a Valve digital signature verified by Windows. Compatible
Steam copies no longer need a separate full-file hash added for each player.
Different game builds or modified game code can still be unsupported.

This update also includes the fixes from 0.6.30:

- Cover selection follows the headset direction instead of the original
  third-person character heading.
- Button throws of canisters and cylinders follow the current hand aim,
  without using a cached backward or sideways swing.
- Audio-buffer allocation recovery handles another crash during mission
  loading or gameplay.
- Weapon grip initialization avoids reusing another item's palm contact
  after a scene or weapon change.
- Earlier SteamVR startup and headset audio fixes are included.

## Updating

Install the complete new package. The installer preserves existing mod settings.
Do not mix launcher, host or mod DLL files from different releases.

## Before playing

This is an early release for Windows. It was tested with the Steam version in
single player. Co-op and multiplayer have not been tested and are not guaranteed.

The original game's 32-bit memory limits remain. Crashes can still occur during
mission loading or gameplay, particularly in long sessions. Some scenery or
textures can disappear, and performance varies between scenes and renderers.

Cover controls can feel awkward. Hold B to enter cover, then use movement with
another B hold to move between cover or vault an obstacle. The first mission
contains a required vault using this mechanic. See [Controls](CONTROLS.md).

One-handed weapons can be transferred to the left hand. Two independent guns
at once and automatic rifle scope zoom are not supported. Grips, reloads,
shadows and scripted interactions can still have visual problems.

See [Installation](INSTALLATION.md) for renderers and headset connections, and
[Known issues](KNOWN-ISSUES.md) for current limitations.
