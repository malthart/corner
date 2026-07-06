# Corner

Keep an eye on your app badges from the macOS menu bar.

**Corner** mirrors the unread badges from your Dock (Mail, Slack, Teams, …) up into
the menu bar — so you don't miss anything while in full-screen mode or on an external
display where the Dock isn't visible.

> **Status:** early work in progress. This repository hosts **releases only** — the
> source is not public.

## Download

Grab the latest build from the [Releases](https://github.com/malthart/corner/releases)
page.

## Requirements

- macOS 14 or later
- Accessibility permission (System Settings → Privacy & Security → Accessibility)

## How it works

macOS doesn't expose other apps' badge counts to third-party apps directly. Corner reads
them through the Accessibility API — each app's unread count is published as the
`AXStatusLabel` attribute on its Dock tile — and polls once a second to pick up changes.

## Acknowledgements

The Dock-badge-via-Accessibility technique was popularised by
[Doll](https://github.com/xiaogdgenuine/Doll). Corner is an independent, clean-room
implementation of the same idea — no code is shared.

## License

Proprietary — all rights reserved. See [LICENSE](LICENSE).
