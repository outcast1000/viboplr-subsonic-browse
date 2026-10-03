# Changelog

## v1.3.0
- **Runs in the plugin worker runtime.** It now gets only what it asks for
  — `network:*`, `playback:read`, `playback:control` — and can't reach anything else in the app. Viboplr asks
  you to allow these once when you update. Requires Viboplr 1.0.85.
- `network:*` because the server is whatever address you type in.

## v1.2.0
- The view header now reflects reality instead of assuming "Connected": on activate every server is pinged in parallel (5s timeout), the header shows "Checking…" until they answer, then Connected / "N of M unreachable" / Unreachable. Searches keep updating it, and adding or editing a server counts as a check. No polling.
- A banner in the Search and Manage tabs names the servers that aren't answering, with a "Check again" button. The Manage list shows "Checking…" per server while its ping is in flight.
- Test harness: vitest 3 → 4.1.11 (fixes GHSA-82fw-gwwq-j7x9 in vitest / @vitest/mocker) and nanoid 3.3.19 (GHSA-2v37-7h3g-55p8). Dev-only; nothing in the plugin zip changes.

## v1.1.0
- The host-drawn view header (Viboplr 1.0.77+) now says which servers you are browsing and whether they answer: "Connected" / "N connected", "1 of 2 unreachable" after a search where some servers failed, "All unreachable" when none did, and "No servers" before you add one. Older hosts are unaffected.

## v1.0.1
- Initial release. Externalized from the Viboplr app's built-in plugins (previously bundled as `subsonic-browse`); functionally identical, now installable and updatable from the plugin gallery.
