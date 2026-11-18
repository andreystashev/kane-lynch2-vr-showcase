# Known issues

These limitations still apply to **0.6.41**.

## Crashes and memory limits

Rare crashes are still reported in the Steam version during gameplay as well
as loading. This update does not resolve them or establish a single cause.

The original game is 32-bit. Its memory limits and built-in integrity checks
restrict what the VR mod can change. Crashes can still occur, most often during
mission loading, but also during gameplay. Long sessions and repeated chapter
changes can be problematic. If a transition crashes, restarting the game and
loading the next chapter from the menu may help.

Some rendering failures open a **Rendering_Setup** dialog on the desktop while
the headset keeps a frozen image. Logged graphics-resource errors and recovery
state help investigate this; the mod does not automatically recover that dialog.
A recorded API error alone does not establish the cause of a freeze or crash.

## Diagnostic logs

In VR settings, enable **Record diagnostic logs** before reproducing a problem,
then restart the mod. Logging is off by default. Each recorded game run keeps
its own folder under `logs/sessions/`, with related game, renderer and VR host
sources. Restarting or turning logging off does not erase earlier sessions.

After a crash or an error, run **Collect-KL2-Diagnostics.cmd** from the mod folder.
It creates a uniquely named ZIP in `diagnostics/`, including the latest five
recorded sessions, available older diagnostic files, package hashes and relevant
Windows crash events from the preceding 48 hours. Send that ZIP with the mod
version, renderer and the action or mission that failed. The export tool also
works after the game has closed and does not start or stop it.

Export limits or unavailable sources are listed in `collection.json`. Individual
logs are bounded, and the export does not delete any source session. Recorded
folders may be removed manually when no longer needed. Logging records
diagnostics and performance history; it does not enable video recording.

## Missing surfaces and texture detail

Some surfaces or objects can disappear and reappear at particular distances.
Texture detail can also change unexpectedly while moving. These issues are
not fully resolved.

## Movement, physical reloading and hands

Default traversal is **hold B to vault**, without entering cover. Physical
peeking and reloads adapt a third-person game; grips, contact points, poses and
scripted interactions can still need adjustment. See [Controls](CONTROLS.md).

Physical leaning adapts the first-person view and visible torso; the original
collision and damage model remain. Clearance protection does not replace that
system. Clipping or unwanted darkening can still occur. Recalibrate with a
0.65-second right stick click hold if the view feels misplaced.

Physical reloading is experimental. Unrecognized mechanisms can retain stock
reload. Ejected magazines are cosmetic and cannot be collected. Helicopter
movement stays within a bounded passenger area, rather than the entire vehicle.

Two independent guns at once and automatic VR rifle-scope zoom remain unavailable.

## Graphics and performance

Performance and stutter remain unresolved. No measured FPS increase or smooth
frame delivery in every scene is claimed for this release.

Frame rate varies between scenes and renderers. Lowering graphics settings or
resolution may help, but CPU limits can remain. See the
[renderer guide](INSTALLATION.md#renderers-and-performance).

New installations render both eye views from one game update in supported
gameplay. Other scenes can use sequential eye updates or a flat display.
Fast motion can still feel less smooth than the headset refresh rate suggests.

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
