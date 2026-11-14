# Kane & Lynch 2 VR 0.6.40

This gameplay update adds physical reloading, physical peeking and direct
vaulting, improves weapon shadows, and makes the helicopter mission more
comfortable to play in VR.

**This remains a pre-release. Rare crashes in the Steam version and unresolved
performance / stutter problems are still reported. This update does not claim
to fix those failures or deliver a measured FPS increase.**

## Physical reloading

- Added manual reloads for supported pistols, revolvers, SMGs, rifles, shotguns
  and machine guns using the game's weapon and magazine geometry.
- Tap **A** to eject a magazine or open a supported cylinder. Use a free hand's
  grip near your shoulder or hip to take a replacement, bring it to the well
  and release. Grip and pull the slide / charging handle when needed.
- A spare can be prepared before ejecting the old magazine. An unused spare
  returns to reserve when released away from the well.
- **Recover ammo from ejected magazines** keeps remaining rounds in reserve,
  or discards them when off. Ejected magazines fall briefly and disappear;
  they cannot be collected. A chambered round remains loaded.
- Improved magazine alignment, insertion, slide targeting, chamber accounting
  and weapon switching. Corrected the initial reload binding of the scripted
  Desert Eagle without needing an extra weapon switch.
- Prevented fore-end support from turning into a magazine grab. Weapon transfer
  now requires about a **two-second receiving-grip hold** with hands together.
- Original reload sounds are read directly from your installed game into memory.
  The mod and source repository contain no game audio files. Generated cues
  remain available if an original cue cannot be read.

**Physical magazine reload (experimental)** is in **Modifiers** and starts enabled
on fresh installations. Explicit existing choices are preserved on update.
Reload-mode changes apply next launch. Unknown mechanisms can retain stock reload;
this does not promise perfect poses for every weapon.

## Peeking and traversal

- Added physical peeking around corners and over obstacles, with bounded
  visible torso movement and closer alignment between the body and headset.
- Removed the original cover-entry sequence from default VR controls. Face an
  eligible low obstacle with the headset and **hold B** to vault, standing or
  crouched. **X** keeps normal interactions.
- **Tap B** to crouch / stand, or press it to get up after being wounded.
- Improved camera settling after movement, weapon contact near walls and doors,
  and headset clearance checks. Original collision and damage still apply.
- Improved hand animation when throwing canisters and cylinders, and hidden
  body-stowed firearms while carrying them.

## Shadows

- Fixed long dark streaks that tracked hand and weapon shadows could produce
  at the shadow area's edge, retaining tracked shadows inside usable bounds.
- Improved head / hair alignment and stationary body-pose handling. Some weapon,
  pose and shadow artifacts can still occur.

## Helicopter mission

- Added stick movement within the moving passenger cabin: approach or back away
  from side openings and move between available sides as cover is damaged.
- Kept movement relative to the helicopter and improved the view during scripted
  turns. Seat-side limits keep the player away from the seating area.
- Preserved the mission's unlimited replacement-magazine supply.

## Updating and remaining issues

Close the game and old settings window, then run **KaneLynch2VR-0.6.40-Setup.exe**.
A portable ZIP is also available. Keep the complete package together; existing
mod settings are preserved. Change graphics and resolution in the game and restart.

The mod targets the **Windows Steam single-player campaign**. Co-op and multiplayer
have not been tested; other editions are not guaranteed. Long sessions, mission
changes, missing surfaces, frame pacing and random crashes remain open issues.
The eye views still come from alternating game frames.

For a failure, enable **Modifiers > Record diagnostic logs**, save and restart,
then run **Collect-KL2-Diagnostics.cmd** after the session. It creates a local
support ZIP and sends nothing automatically.

See [Installation](https://github.com/andreystashev/kane-lynch2-vr-showcase/blob/main/INSTALLATION.md),
[Controls](https://github.com/andreystashev/kane-lynch2-vr-showcase/blob/main/CONTROLS.md)
and [Known issues](https://github.com/andreystashev/kane-lynch2-vr-showcase/blob/main/KNOWN-ISSUES.md).
