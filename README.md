RadClock Canvas easy-install edition

Use Clockwise's Canvas clockface and host radclock.json on a reachable HTTPS server.
Set Canvas Server Address to that host and Canvas Description file to: radclock

Behavior:
- Live HH:MM in the top sign
- Tube, patient, and computer monitor
- No detector
- Monitor shows a small chest X-ray when idle
- Repeating ~60-second visual cycle: 55s idle, 3s beam, 2s post-exposure

Canvas limitation:
The JSON loop is delay-based, not tied to the real minute boundary, and it cannot
conditionally replace the live datetime with X-RAY ON. The native C++ version is
still required for exact TIME -> flashing X-RAY ON -> updated TIME behavior.
