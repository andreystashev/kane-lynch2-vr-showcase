# Installation

These instructions apply to Kane & Lynch 2 VR **0.6.39**.

You need Windows 10/11 x64, a PC VR headset and your own copy of **Kane & Lynch 2:
Dog Days**. This release was tested with the Windows Steam version. Other game
editions and modified executables are not guaranteed to work.

## Install and launch

1. Install and run the game normally through Steam at least once.
2. Connect the headset using its PC application.
3. Run the VR mod installer. Use a separate mod folder, outside the game folder.
4. Open **Kane & Lynch 2 VR Settings**. Steam libraries are searched
   automatically; use **Find game** or select `kl2.exe` if needed.
5. Choose the connection and renderer, then use **Save & play**.

After setup, the **Kane & Lynch 2 VR** shortcut starts the game with your saved
choices. **Kane & Lynch 2 VR Settings** opens the settings window.

The portable ZIP is an alternative to the installer. Extract it into a separate
folder and open `KaneLynch2VRSettings.exe`. Keep all package files together.
The game is rediscovered on another PC; use **Find game** if its location changes.

## Headset connection

Choose the connection you are actually using, separately from the game renderer:

| Connection | Use with |
| --- | --- |
| Automatic | Automatic selection of an installed PC VR runtime. |
| Quest Link / Air Link (Meta) | The Meta Quest Link PC application. |
| Virtual Desktop (VDXR) | Virtual Desktop Streamer with VDXR selected. |
| SteamVR / Steam Link | A headset connected through SteamVR. |
| OpenXR | Your active OpenXR runtime, or an optional runtime JSON file. |

Start the corresponding PC VR application and connect the headset before
launching the mod. If Automatic chooses a different connection, select yours
explicitly. Leave the optional OpenXR runtime file blank for normal use.
Support can vary between headset and controller models.

## Renderers and performance

| Renderer | What to expect |
| --- | --- |
| **D3D9On12** (default) | Runs the game through Direct3D 12 and uses GPU image transfer when available. Start with this option. Requires Windows support for D3D9On12. |
| **DXVK** | Runs Direct3D 9 through Vulkan. Requires a Vulkan-capable graphics driver. Performance varies by system. |
| **Original** | Uses the game's Direct3D 9 renderer. Useful for comparing compatibility and performance. |

VR image transfer can use more CPU time with Original and DXVK than with the
D3D9On12 GPU path. The original game can also be limited by the CPU, so lowering
resolution does not always improve frame rate. Compare renderers in the same
scene at the same settings; none is fastest on every PC.

This release reduces image copies and repeated CPU work, but a specific FPS
gain is not guaranteed. The eyes are still updated on alternating game frames;
two fresh eye views from the same game state are not yet available.

Set resolution and graphics quality **inside the game**, then restart it.
Always close the game before selecting another renderer. Renderer changes
take effect on the next launch. Existing ReShade or other renderer files may
conflict with switching; the launcher reports this instead of replacing them.

## Diagnostic logs

Logging is **off by default** on a fresh installation. To collect information
about an intermittent crash, freeze or stutter:

1. Open **Kane & Lynch 2 VR Settings → Modifiers** and enable
   **Record diagnostic logs**.
2. Save the settings, then launch or restart the game. The option applies to
   the next session.
3. After the problem occurs, close the game if it is still running. Run
   **Collect-KL2-Diagnostics.cmd** from the mod folder.
4. Find the new `KL2-diagnostics-...-support.zip` in the mod's `diagnostics/`
   folder. Include it with your issue report, together with the mission,
   renderer, headset connection and a description of what happened.

Logs from separate sessions are kept under `logs/sessions/`, so you can collect
them after the game has exited. Individual logs have size limits, and the
collector exports a limited selection of recent sessions. Turning logging off
does not delete earlier logs. Old session folders and collected ZIPs are kept
until you remove them.

The logs include frame timing, graphics-resource errors and observed rendering
failures. They can help investigate a problem but may not identify its cause.
Video recording is not required or enabled by this option. The collector does
not start or close the game, and it does not send anything automatically.
Review the archive before sharing it publicly.

## Updates and removal

Close the game before updating or uninstalling. Updates keep your mod settings;
the installer does not replace the game executable or saved games.

Uninstall through **Windows Settings > Apps**. Your mod configuration is kept.
An optional renderer installed beside the game is kept too. To return the game
to its original renderer, choose **Original**, launch once and close the game
before uninstalling the mod.
