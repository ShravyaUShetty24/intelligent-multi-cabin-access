# Technical Case Study — Intelligent Multi-Cabin Access System

## Context and challenge
The project manuscript identifies the limits of mechanical keys, single-door access solutions and the lack of remote owner approval. The proposed academic prototype combines a Raspberry Pi controller, camera, automatic electronic locks and Telegram communication for multi-cabin access.

## Implemented workflow (as reported)
1. A Raspberry Pi camera or attached webcam captures an approaching user's face.
2. Haar Cascade detects the face; the LBPH recognizer compares it against enrolled samples.
3. For a known authorized user, the Raspberry Pi GPIO controls a relay that energizes or releases the assigned solenoid lock.
4. For an unrecognized person, the system captures a photograph and sends it to the cabin owner using a Telegram bot.
5. The cabin owner can respond remotely to approve or deny access.
6. LCD/buzzer messages and access logs provide local feedback and an audit trail.

## Components
- Raspberry Pi computer and Pi-compatible camera
- Relay module, solenoid lock, power supply, LCD display and buzzer
- Python, OpenCV, Haar Cascade and LBPH
- Telegram Bot API for remote messages and owner decisions

## Evidence supplied
- A photograph of the prototype wiring documents the Raspberry Pi, power interface, relay and solenoid.
- Screenshots from the Raspberry Pi desktop and Thonny editor document face data collection and recognition demonstrations.
- Messaging screenshots document alerts and owner response messages.
- A seven-page academic research manuscript includes the system architecture, modules, results, photographs, technologies and future improvements.

For safety, this public repository does **not** include identifiable face samples, the chat screenshots, code screenshots showing secret tokens, or raw training datasets. A sanitized evidence gallery can be added later with all participants' consent.

## What was observed vs. not independently verified
The project authors report successful recognition and prototype operation under different lighting and angles. The supplied materials do not establish a reproducible public benchmark, a production threat-model audit, or verified reliability over extended deployments. Thus no unsupported accuracy or uptime percentage is advertised here.

## Next improvements proposed in the paper
Liveness detection, multi-factor authentication, stronger encryption, local/offline operation, audit dashboard, expanded cabin control and monitoring.

## Security maintenance
If previously used Telegram Bot API tokens appear in screenshots or code, treat them as compromised, revoke them using BotFather and rotate any affected credentials.

## Portfolio profile
**Shravya U Shetty** — academic project contributor and portfolio owner, Acharya Institute of Technology. This page highlights her documented work without claiming sole authorship of all components.
