# Known issues

These limitations still apply to **0.6.39**.

## Crashes and memory limits

The original game is 32-bit. Its memory limits and built-in integrity checks
restrict what the VR mod can change. Random crashes can still occur, most often
during mission loading, but also during gameplay. Long sessions and repeated
chapter changes can be problematic. If a transition crashes, restarting the
game and loading the next chapter from the menu may help.

Some rendering failures open a **Rendering_Setup** dialog on the desktop while
the headset keeps showing a frozen image. This release adds logging for failed
graphics-resource requests and the game's rendering-recovery state; it does
not fix every failure or automatically recover from that dialog. A recorded
API error alone does not establish the cause of a freeze or crash.

For an intermittent failure, enable logs **before** the next session, then
collect them after closing the game. See [Diagnostic logs](INSTALLATION.md#diagnostic-logs).
There is no need to record video or repeatedly replay a mission just to gather
logs from a failure that has already been recorded.

## Missing surfaces and texture detail

Some surfaces or objects can disappear and reappear at particular distances.
Texture detail can also change unexpectedly while moving. These issues are
not fully resolved.

## Movement, cover and hands

This is a VR adaptation of a third-person game. Cover and scripted interactions
can feel awkward; some poses, grips, reloads and shadows can look unnatural.
Follow the [cover controls](CONTROLS.md) when vaulting or moving between cover.

Physical leaning does not move the character's collision body, so the camera
can clip through nearby walls. Recalibrate VR height and body position with a
0.65-second hold of the right stick click if the view feels misplaced.

One-handed weapon transfer is available, but two independent guns at once are
not supported. Automatic scope zoom by bringing a rifle to the headset is not
available.

## Graphics and performance

Frame rate varies between scenes and renderers. Lowering graphics settings or
resolution may help, but CPU limits can remain. See the
[renderer guide](INSTALLATION.md#renderers-and-performance).

The OpenXR and CPU optimizations in this release reduce specific overheads;
there is no matched before-and-after FPS result or guaranteed frame-rate gain.
The eyes are still updated on alternating game frames, rather than both being
rendered freshly from one game state. Fast motion and head turns can therefore
feel less smooth than the headset's refresh rate suggests.

Changing graphics settings can leave a frozen image in the headset or disrupt
the hands. Restart the game after changing them. Close the game before changing
its renderer in mod settings.

## Launch and audio troubleshooting

- If setup reports an unsupported executable, include the SHA256 shown in the
  message and the game's Steam Build ID when reporting the problem.
- Steam copies with different full-file hashes can be recognized when their
  supported game code and native data match and Windows verifies Valve's
  digital signature. Different game builds still require compatibility work.
- If SteamVR opens only the desktop game window in version 0.6.25, update the
  complete mod to 0.6.26 or newer. Do not mix files from different versions.
- If Steam stays on **Launching**, check for a pending Steam launch choice. In
  the game's Steam properties, choose **Play Kane & Lynch 2** rather than
  **Ask when starting** if the choice never appears.
- If a launcher file disappears or startup is blocked, check your security
  software's protection history. Windows Defender quarantined the launcher in
  version 0.6.24. Include the warning and mod version when reporting a problem.
- Connect the headset before starting the game. If sound remains on the PC,
  check the selected connection and restart the game. SteamVR audio mirroring
  can also play sound on PC speakers while headset audio is working.

## Compatibility

This release was tested with the Windows Steam version in single player.
Co-op and multiplayer have not been tested; their operation is not guaranteed.
Compatibility and controller behaviour can vary between headsets and PC VR
applications.
