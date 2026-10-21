# Implementation Insights — Intelligent Multi-Cabin Access System

## Academic evidence
The team manuscript *Intelligent Multicabin Access System Using Face Recognition* describes a Raspberry Pi-based prototype using a camera, Haar Cascade face detection, LBPH recognition, electronic locking and Telegram owner alerts. Screenshots show hardware wiring, camera/recognition output and chat alerts. The source code has not been shared for public publication.

## Shravya's described contribution
In the supplied `intelli.pdf` interview notes, Shravya describes:
- Working on **OpenCV face acquisition and Haar Cascade detection**.
- Training an **LBPH recognizer** using face samples.
- Connecting **Raspberry Pi GPIO** to the relay and solenoid lock.
- Implementing **Telegram image alerts and remote approval/denial**.
- Testing and debugging lighting, multi-face input and hardware interfacing.

These are **Shravya U Shetty's reported contributions**, not a verified commit history. The source paper documents a collaborative student project with faculty guidance; the portfolio focuses on Shravya's own work.

## Workflow in the supplied material
1. Camera video is captured on the Raspberry Pi; frames are converted to grayscale for face detection.
2. Haar Cascade locates faces; a trained LBPH model returns a recognition decision/confidence score.
3. An accepted face triggers GPIO → relay → electronic solenoid lock.
4. Unrecognized faces trigger saved image evidence and a Telegram notification.
5. The cabin owner may approve or deny remotely; the system may show an LCD message or sound a buzzer.

## Reported engineering challenges
- **Lighting changes:** the interview notes describe additional training samples and grayscale preprocessing.
- **Multiple faces:** the notes report using the primary detected face.
- **False accepts:** recognition threshold adjustment is described; no reproducible validation results were supplied.
- **Telegram reliability:** message delay and retry ideas are described; robustness has not been independently demonstrated.

## Technical considerations
The Raspberry Pi GPIO is not suitable for driving a 12V solenoid directly, so a relay/power supply is used. The screenshots show the prototype hardware layout. The paper qualitatively reports successful authorized/unknown-user handling; it does not include reproducible accuracy metrics.

## Security and responsible handling
**A screenshot shows a live-looking Telegram token. Revoke the token with BotFather and rotate it.** Do not publish facial biometric datasets, raw photo evidence or personal chat IDs without consent. Before real deployment, add liveness detection, authorization hardening, safer token management and a safe lock-failure policy.

## Sources
Team research paper and `intelli.pdf` interview-preparation notes, supplied by the project team. The original PDFs and biometric screenshots are not redistributed in this repository.
