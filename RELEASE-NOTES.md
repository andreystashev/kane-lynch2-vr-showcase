# Kane & Lynch 2 VR 0.6.39

This update improves VR projection, menus and subtitles, reduces rendering and
CPU overhead, and adds optional diagnostics for intermittent problems.

## Picture, menus and subtitles

- Fixed a projection mismatch when the game letterboxes its output. It could
  make the world distort or appear to swim as you turned your head.
- In-mission pause menus now open on a flat VR panel. Panels fit within the
  headset's field of view and use a farther default distance, so menus and
  loading screens stay manageable after resolution or video-setting changes.
- Restored the game's own gameplay subtitles when enabled in its settings,
  with a small shift to the right for VR. Unwanted legacy HUD hints remain hidden.

## Rendering and performance

- Reduced intermediate OpenXR image copies and reused render-target views
  and full-eye geometry instead of rebuilding them for each submission.
- Removed redundant GPU flushes and an extra HUD capture copy.
- Reduced repeated CPU work for skeleton metadata, weapon-mesh checks and HUD
  buffers while keeping resource and ownership checks.
- Moved diagnostic process sampling and file writes away from the compositor
  loop and limited the amount of diagnostic work.

There is no matched before-and-after FPS result for this release. Performance
still varies by scene, renderer, resolution and PC, and stutter remains possible.
The eyes are still rendered on alternating game frames; two fresh eye views
from the same game state are not yet implemented.

## Optional diagnostic logs

**Record diagnostic logs** is available under **Modifiers** in the settings
window. It is off on a fresh installation. Enable it, save the settings and
restart the game before a session you want to record.

The logs retain information from separate sessions, including frame timing,
failed Direct3D resource requests and observed rendering-recovery errors.
Individual logs have size limits. Earlier sessions are not erased at startup
or when logging is turned off.

After a failure or normal exit, run **Collect-KL2-Diagnostics.cmd** from the mod
folder. It creates a new `KL2-diagnostics-...-support.zip` in `diagnostics/`
with a limited selection of recent sessions. No video is required. The
collector does not launch or close the game and does not upload anything.
Review the archive before attaching it to an issue report. Old logs and ZIPs
remain until you remove them.

These diagnostics help investigate random failures; they do not guarantee a
diagnosis or automatically recover the game. A graphics API error recorded near
a failure is not necessarily its cause.

## Updating

Close the game and the old settings window, then install
`KaneLynch2VR-0.6.39-Setup.exe`. A portable ZIP is also available. Use the complete
package and keep its files together. Existing mod settings are preserved.

Set resolution and graphics quality inside the game, then restart it. Close
the game before changing renderers in the mod settings.

## Remaining limitations

- Random crashes and **Rendering_Setup** errors can still occur during mission
  loading and sometimes during gameplay. A rendering error can leave the
  headset image frozen while a dialog is open on the desktop. Long sessions
  and repeated mission changes remain a concern within the game's 32-bit
  memory limits.
- Some surfaces, objects and texture detail can still disappear or change at
  particular distances.
- Cover, vaulting and scripted interactions can be awkward in VR. Hold **B**
  to enter cover, release it to stay there, then use another **B hold with the
  left stick** to move between cover or vault. Tap B to leave. The first
  mission contains a required vault using this mechanic.
- Eligible one-handed guns can be transferred to the left hand. Two
  independent guns at once and automatic VR rifle-scope zoom remain unavailable.
  Grips, reloads, poses and shadows can still have visual problems.

The mod is intended for the **Windows Steam single-player campaign**. Other
editions are not guaranteed to work. Co-op and multiplayer have not been run
or tested and are not guaranteed to work. Headset and controller compatibility
can vary with the selected PC VR runtime.

See [Installation](https://github.com/andreystashev/kane-lynch2-vr-showcase/blob/main/INSTALLATION.md),
[Controls](https://github.com/andreystashev/kane-lynch2-vr-showcase/blob/main/CONTROLS.md)
and [Known issues](https://github.com/andreystashev/kane-lynch2-vr-showcase/blob/main/KNOWN-ISSUES.md)
for setup and current limitations.
