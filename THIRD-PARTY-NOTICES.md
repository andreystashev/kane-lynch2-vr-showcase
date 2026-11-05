# Third-party notices

This package includes the project's own mod runtime and launcher. It does not
include Kane & Lynch 2 game assets or a Microsoft Direct3D runtime.

- DXVK: zlib license; see renderer-dxvk-x86/LICENSE and provenance.json.
- D3D9On12 selector: owned selector for the Windows system implementation;
  see renderer-d3d9on12-x86/NOTICE.txt and MINHOOK-LICENSE.txt.
- MinHook: BSD 2-clause; see licenses/MinHook-LICENSE.txt.
- Oculus/Meta API declarations: see licenses/Oculus-SDK-LICENSE.txt.
- OpenXR loader and JsonCpp notices accompany the loader when included.
- OpenVR API declarations for SteamVR audio-device queries: see OPENVR-LICENSE.
  The OpenVR DLL is loaded from the user's installed SteamVR and is not bundled.
- LLVM-MinGW static runtime components: see the respective files in licenses/.
- Audio routing support: see THIRD-PARTY-AUDIO.txt.

The installer uses Inno Setup. Windows and headset runtimes must be installed
separately from their original vendors.
