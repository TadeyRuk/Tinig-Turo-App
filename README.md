# Tinig-Turo (Android)

**Sound you can see.** Tinig-Turo tells Deaf and Hard-of-Hearing users **what** a sound is and **where** it is coming from, live on an Android phone. It pairs GCC-PHAT sound-source localization with YAMNet sound classification, and shows direction and sound type as simple visual cues.

Built by **Project Kensho** at the FEU Institute of Technology.
Paper: *Tinig-Turo: A Computational Sound Localization and Semantic Classification System with GCC-PHAT and YAMNet.*

Website: **https://tinigturo.vercel.app/**

## Download

Get the latest APK from the **[Releases page](../../releases/latest)** and install it on your phone.

### Install steps

1. Open the Releases page on your Android phone and download `app-release.apk`.
2. Open the downloaded file. If Android asks, allow your browser or Files app to **install unknown apps** (Settings > Apps > Special access > Install unknown apps).
3. Tap **Install**, then open **Tinig-Turo**.
4. Grant the **Microphone** permission, and the **Notifications** permission on Android 13 or newer. Direction detection and alerts need both.

To check your download, compare its SHA-256 with the one listed in the release notes.

## Requirements

| | |
|---|---|
| Android | 8.0 or newer. Developed and evaluated on Android 14+. |
| Microphones | **Two working microphones.** Direction estimation needs both. |
| Download size | About 95 MB |

## How it works

- **Where:** two microphone signals are compared with GCC-PHAT to estimate the direction of a sound.
- **What:** YAMNet, a MobileNetV1 model trained on AudioSet, classifies sounds across 521 categories.
- **Fusion:** a confidence-based layer prioritizes safety-critical sounds such as sirens and alarms, then shows the result as a direction and a label.
- Audio is processed on the device.

## Limits

- Tinig-Turo is an **assistive tool, not a medical or safety device.** Do not rely on it for situations where missing a sound could cause harm.
- Direction is a **best-effort estimate**, not a pinpoint. Phone microphones sit close together, so accuracy drops in echoey rooms and at extreme side angles.
- It was evaluated in controlled and semi-controlled conditions with a purposive sample of 20 respondents.

## Source code

The source code is **not published** in this repository. This repo only hosts the downloadable app and its release notes.

## Feedback

Found a problem or have a suggestion? Open an [issue](../../issues) and include your phone model and Android version.

## Acknowledgments

Thanks to our mentor Mr. Justine Jude C. Pura, our co-mentees, Mr. Vins Balingan, the Hard of Hearing Group Philippines (HOHGP), the FEU Institute of Technology faculty, and DOST-SEI.
