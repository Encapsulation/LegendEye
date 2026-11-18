![LegendEye](docs/hero_v5.png)

https://github.com/user-attachments/assets/e355732c-f763-4491-8cbc-104bee171a90



https://github.com/user-attachments/assets/6669fe4a-ca21-4385-8b5a-49e3ea01fefb

# LegendEye


Eye tracking, face tracking and dynamic foveated rendering for the **Bigscreen Beyond 2e**. Free to use.

## What's new in 5.0

Your existing calibration keeps working. Recalibrate to get the new improvements. Simple calibration with the default settings is recommended.

### Dynamic foveated rendering (DFR)
- LegendEye now sends your gaze to SteamVR through its own driver, so games with built-in eye-tracked foveated rendering use it directly (for example iRacing and Microsoft Flight Simulator 2024).
- LegendQuad, our own quad-views layer, adds eye-tracked foveated rendering to games that support quad views, such as DCS World.
- Quality, Balanced and Performance presets, plus Advanced sliders for sharp area size, outer detail, edge blend, sharpening, shape, vertical offset and hold time.
- Brightness match keeps the sharp area and the outer view the same brightness, so the edge is harder to see.
- LegendQuad only runs in games you start with LegendEye's Steam launch option or its "Launch with LegendQuad" button.
- Launch with LegendQuad finds your Steam games automatically. Add a game adds any other game.
- Warning: LegendQuad is recommended for single-player or offline games. Anti-cheat can flag or ban accounts for files loaded into a game, even ones that aren't cheats. LegendQuad blocks games with Easy Anti-Cheat or BattlEye unless you choose Allow anyway, at your own risk.
- Gaze for foveation tools over OSC, such as PimaxMagic4All.

### Face tracking
- Face tracking with the VIVE Facial Tracker and Babble cameras, using the Babble model, the VIVE model, or both blended.
- Both (blend) trusts whichever model reads each face shape best.
- Copy model buttons keep your own installed Babble or VIVE model inside LegendEye, so you can uninstall those apps afterward.
- Face smoothing with a low lag to smooth slider and per-part strength.
- Face output ranges let you set the range and maximum sent for every face shape.
- Sends to VRChat directly, through VRCFaceTracking, or to other apps.

### LegendPanel
- Works with [LegendPanel](https://github.com/Encapsulation/LegendPanel), our new standalone VR performance panel.
- LegendEye remote: pause, resume, recenter, face tracking, expressions, sending to the game, and foveated rendering presets from inside VR.
- LegendEye feeds LegendPanel's eye-tracked menu.

### Calibration and recenter
- Recenter with 1 or 5 dots, offered when you put the headset on (on by default, 1 dot, click to start, adjustable wait).
- Optional extra blinks step (off by default): close gently and squeeze at 5 or 9 dots, for eyes that open by themselves when shut.
- Brows: Off, Short brows (default, frown and brows up at 5 dots so widen and squint ignore your brows) or full Brows.
- Advanced uses 5 expression dots by default, or 9 if you pick it.
- Named calibrations: every calibration is kept, and you can switch, rename or delete them on the Profiles tab.
- All calibration dots use the same crosshair.

### Tracking
- Frowning and squinting pull your gaze off much less.
- Closed eyes stay closed, and squeezing your eyes shut reads properly.
- Raising or lowering your brows no longer shows up as widen or squint.

### App
- New Face and DFR tabs.
- Memory protection: LegendEye waits or switches to the CPU instead of starting heavy work when your PC is low on memory.
- Lower CPU use.

Updating: replace LegendEye.exe. Your settings and calibrations are kept.

## Download
Get **LegendEye.exe** from the [latest release](https://github.com/Encapsulation/LegendEye/releases/latest). It's a single file: no installer, nothing to unpack.

> Windows may show "Windows protected your PC" the first time, because the app isn't code-signed yet. Click **More info**, then **Run anyway**.

> **VirusTotal (v5.0.0):** [report](https://www.virustotal.com/gui/file/8f7dcdfef6f039bed1337bf4a66321a469b3702b30d521035c6594091df279cd)  
> SHA256: `8f7dcdfef6f039bed1337bf4a66321a469b3702b30d521035c6594091df279cd`

## Requirements
- Windows 10 or 11 (64-bit)
- Bigscreen Beyond 2e with its eye-tracking cameras
- SteamVR
- Turn off the eye tracking in the Bigscreen driver or software and close any other eye-tracking app. Only one app can use the cameras at a time.

## Getting started
1. Run LegendEye.exe and press **Start**. It talks to VRChat directly (OSC), with no extra software needed.
2. Press **Calibrate**, pick **Simple** or **Advanced**, and tick the expressions to set up (widen, squint, brows). Follow the voice: keep your head still and follow the dot with your eyes. Simple takes about 3 minutes; then your personal eye model trains automatically and is used from then on.
3. Optional: let LegendEye start with SteamVR. It then waits in the tray, ready whenever you are.

> Check the eye camera feeds in LegendEye before each session. The white glow near the edges is normal; dust, skin, and other contamination and debris near the center can cause issues, especially during calibration. If the center isn't clear, a lens puffer brush works best. Otherwise wipe gently with the included microfiber cloth; for stubborn debris, wrap the cloth over a blunted toothpick. Never use liquids or cleaning agents.

## Features
- Gaze, eyelids (with winks and blinks) and pupil size for any VRChat avatar with eye tracking
- Widen, squint and brows, set up for your eyes in your calibration, each with its own switch, sensitivity, start point and output range
- A head-still calibration that personalizes the eye model to you: Simple, or Advanced with paths fitted to your gaze range
- Field of view check: how far your eyes turn and what each eye sees, as a report
- Settings profiles, and a Reset button on every settings card
- Easy mode with live readouts; Advanced mode with filters, per-eye lid tuning (closed / open levels), horizontal and vertical eye movement scale and limit, near convergence, and the avatar's pupil size and reaction
- Closes the avatar's eyes when the headset is taken off
- Skips torn camera frames when the USB cable loses data
- Camera reconnects by itself after a USB drop or a headset replug
- Pauses when SteamVR closes and resumes by itself
- Dirty-lens warning
- Optional calibration report in Export logs, so tracking problems can be fixed for your eyes
- Runs on the GPU by default (DirectML: NVIDIA, AMD or Intel), with automatic CPU fallback; pick the GPU or the CPU in the settings

## Using LegendEye with Babble (VRCFaceTracking)
LegendEye talks to VRChat on its own. If you also use a mouth tracker such as Babble through VRCFaceTracking (VRCFT), install the LegendEye VRCFT module, so VRCFT combines LegendEye's eyes with Babble's mouth. VRChat accepts only one face tracking message at a time: without the module, the two overwrite each other.
1. Download `LegendEye-VRCFT-Module-1.1.0.zip` from the [module release](https://github.com/Encapsulation/LegendEye/releases/tag/vrcft-module-1.1.0) and install it in VRCFT: **Module Registry**, then the **Install from .zip** button next to the search box. Avatars set up for VRChat's native face tracking need a VRCFT version that sends it.
2. In LegendEye, click **Advanced** (top right), open the **Output** tab, and in the **VRChat** box set **OSC port** to `9400` and **Native face** to **Always**.
3. In VRCFT, uninstall or disable **Bigscreen's Beyond module** (it would take the eyes), and keep **LegendEye above Babble** in the module list. In Babble, turn its own eye tracking off. VRCFT's log shows whether LegendEye data arrives.
4. Start LegendEye, Babble and VRCFT. Eyes, blinks and pupils come from LegendEye, the mouth from Babble. VRCFT adds about 6 ms; without a mouth tracker, keep the normal setup (no module) for the lowest latency.

## Help
- Report problems at [Issues](https://github.com/Encapsulation/LegendEye/issues). In the app, click **About** and then **Export logs**, and attach the zip.

## License
Free to use; all rights reserved. See LICENSE.txt. Third-party components are listed in THIRD_PARTY_NOTICES.txt.

## Star History
<a href="https://www.star-history.com/#Encapsulation/LegendEye&Date">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Encapsulation/LegendEye&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Encapsulation/LegendEye&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Encapsulation/LegendEye&type=Date" />
  </picture>
</a>
