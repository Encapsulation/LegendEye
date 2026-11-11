

https://github.com/user-attachments/assets/e355732c-f763-4491-8cbc-104bee171a90

# LegendEye

![LegendEye](docs/hero_v2.png)

Eye tracking for VRChat on the **Bigscreen Beyond 2e**. Free to use.

## Download
Get **LegendEye.exe** from the [latest release](https://github.com/Encapsulation/LegendEye/releases/latest). It's a single file: no installer, nothing to unpack.

> Windows may show "Windows protected your PC" the first time, because the app isn't code-signed yet. Click **More info**, then **Run anyway**.

> **VirusTotal (v3.0.0):** [1 of 69 security vendors flagged it](https://www.virustotal.com/gui/file/fdf709662fbb63d1f9fc876e257bce8d390b28f6c70fc943e5013bddbd146a8f).  
> SHA256: `fdf709662fbb63d1f9fc876e257bce8d390b28f6c70fc943e5013bddbd146a8f`

## Requirements
- Windows 10 or 11 (64-bit)
- Bigscreen Beyond 2e with its eye-tracking cameras
- SteamVR
- Turn off the eye tracking in the Bigscreen driver or software and close any other eye-tracking app. Only one app can use the cameras at a time.

## Getting started
1. Run LegendEye.exe and press **Start**. It talks to VRChat directly (OSC), with no extra software needed.
2. Press **Calibrate** and follow the voice: keep your head still and follow the dot with your eyes. It takes about 2.5 minutes, then your personal eye model trains automatically and is used from then on.
3. Optional: let LegendEye start with SteamVR. It then waits in the tray, ready whenever you are.

> Check the eye camera feeds in LegendEye before each session. The white glow near the edges is normal; dust, skin, and other contamination and debris near the center can cause issues, especially during calibration. If the center isn't clear, a lens puffer brush works best. Otherwise wipe gently with the included microfiber cloth; for stubborn debris, wrap the cloth over a blunted toothpick. Never use liquids or cleaning agents.

## Features
- Gaze, eyelids (with winks and blinks) and pupil size for any VRChat avatar with eye tracking
- A head-still calibration that personalizes the eye model to you
- Easy mode with live readouts; Advanced mode with filters, per-eye lid tuning (closed / open levels), horizontal and vertical eye movement scale and limit, near convergence, and the avatar's pupil size and reaction
- Closes the avatar's eyes when the headset is taken off
- Skips torn camera frames when the USB cable loses data
- Camera reconnects by itself after a USB drop or a headset replug
- Pauses when SteamVR closes and resumes by itself
- Dirty-lens warning
- Optional calibration report in Export logs, so tracking problems can be fixed for your eyes
- Runs on the GPU by default (DirectML: NVIDIA, AMD or Intel), with automatic CPU fallback

## How the numbers were measured
- Gaze: one tester on one Beyond 2e, 9 dots per session, with every app scored after the same per-axis fit on the other 8 dots. LegendEye is two sessions pooled, using its personal calibration. Babble used an older per-user calibration.
- Blink detail: the in-between eyelid levels each app sent per eye during 10 cued blinks, averaged across both eyes. One tester. Bigscreen sends one shared value for both eyes.
- Internal latency: camera frame to VRChat-ready. Bigscreen's figure is only the output hand-off that can be measured, so its true total is higher. PaperTracker's is estimated from a dot-jump test.

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
