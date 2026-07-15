<p align="right">English · <a href="README.zh.md">中文</a></p>

<p align="center">
  <img src="docs/screenshots/icon.png" alt="Tutti app icon" width="128" height="128">
</p>

<h1 align="center">Tutti</h1>

<p align="center"><em>One sound, every speaker.</em></p>

<p align="center">The menu bar audio control center macOS never shipped —<br>multi-output, per-app volume &amp; EQ, Now Playing, and an iPhone remote.</p>

<p align="center">
  <a href="https://github.com/BarryBarrywu/tutti/releases/latest/download/Tutti.dmg"><strong>⬇︎ Download for macOS</strong></a>
  ·
  <a href="https://tutti.barrybarrywu.com">Website</a>
  ·
  <a href="https://github.com/BarryBarrywu/tutti/releases">Releases</a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/BarryBarrywu/tutti?style=flat-square&color=blue&label=release" alt="Release">
  <img src="https://img.shields.io/badge/macOS-13.0+-000000?style=flat-square&logo=apple&logoColor=white" alt="macOS 13+">
  <img src="https://img.shields.io/github/downloads/BarryBarrywu/tutti/total?style=flat-square&color=orange&label=downloads" alt="Downloads">
  <img src="https://img.shields.io/badge/Pro-$7.99_one--time-38bdf8?style=flat-square" alt="Pro $7.99 one-time">
</p>

<p align="center">
  <img src="docs/screenshots/panel.webp" alt="Tutti menu bar panel in light and dark" width="720">
</p>

<p align="center"><sub><strong>No virtual driver · no system extension · no telemetry · no account.</strong> Notarized by Apple. Quit Tutti and your audio setup is exactly as it was.</sub></p>

## Why Tutti

macOS gives you a volume slider, a device list, and a tiny speaker glyph — and that's it. You can't play to two speakers at once, can't set a different volume per app, can't EQ one app without touching the rest. Tutti is the control center that fills the gap: one panel for every output, every app, and every level — riding Apple's own audio frameworks, with nothing installed into your system.

<p align="center">
  <img src="docs/screenshots/mac-per-app-eq.webp" alt="Per-app equalizer curve" width="230">
  &nbsp;
  <img src="docs/screenshots/mac-stereo-split.webp" alt="Stereo pairing across devices" width="230">
  &nbsp;
  <img src="docs/screenshots/mac-latency-balance.webp" alt="Per-device latency and balance" width="230">
</p>

<p align="center"><sub>Draggable per-app EQ · stereo pairing across two speakers · per-device latency &amp; balance.</sub></p>

## 📱 Tutti Remote — now on the App Store

**Control your Mac's audio from your iPhone.** Sit on the couch and switch presets, pick output speakers, set per-device and per-app volume, and drive playback from an iPod-style click wheel. Pairs over your local network; the Mac stays in charge. The iPhone app is free; controlling your Mac needs Tutti Pro there.

<p align="center">
  <a href="https://apps.apple.com/app/tutti-remote/id6788375184"><strong>Download Tutti Remote on the App Store →</strong></a>
</p>

<p align="center">
  <img src="docs/screenshots/ios-now-playing.png" alt="Tutti Remote — Now Playing" width="240">
  &nbsp;&nbsp;
  <img src="docs/screenshots/ios-devices.png" alt="Tutti Remote — Devices and presets" width="240">
  &nbsp;&nbsp;
  <img src="docs/screenshots/ios-app-volume.png" alt="Tutti Remote — per-app volume" width="240">
</p>

## Features

### Multi-device output
- **Play to every speaker at once** — tick multiple outputs and Tutti builds a CoreAudio Aggregate Device on the fly, keeping them clock-synced.
- **Or just one** — pick a single device and Tutti switches the system default directly, no aggregate created.
- **Master + per-device volume & mute** — one slider for everything, plus an individual slider and mute for each output.
- **Three-state status** — playing on all, partially muted, or all muted, with a matching color dot.
- **Hot-swap without a gap** — add or remove a speaker mid-playback without cutting the sound.
- **Device Guard** — set a priority order for your outputs and lock the default output, input, and volume; when macOS or another app switches them behind your back, Tutti puts them back.
- **Remembers your setup** — your speaker group, per-device volumes, and mute survive quitting Tutti and app updates.

### Per-app audio control &nbsp;`macOS 14.4+`
- **Per-app volume & Turbo** &nbsp;`Free` — give each app its own level; Turbo adds a 2× boost. Driver-free, via a native audio tap.
- **Per-app equalizer** &nbsp;`Free` — a draggable 6-band EQ curve for any app, or a built-in preset.
- **Per-app output** &nbsp;`Pro` — send different apps to different speakers; keep a call on the laptop while music fills the room.
- **See where sound goes** — output devices show small badges of the apps routed to them.
- **Ignore apps you don't manage** — right-click any app to tuck it out of the list.

### Pro power tools
- **Presets** &nbsp;`Pro` — save device + volume + per-app combos and switch with one click; each gets its own emoji.
- **Global keyboard shortcuts** &nbsp;`Pro` — hotkeys to open the panel, mute, switch preset, or nudge an app's volume from inside any app.
- **Stereo pairing across devices** &nbsp;`Pro` — send the left channel to one speaker and the right to another — two speakers, one stereo pair.
- **Per-speaker left-right balance** &nbsp;`Pro` — lean any speaker's sound toward one side when it sits off-center.
- **Per-device latency tuning** &nbsp;`Pro` — dial in a small delay, by ear, for a Bluetooth speaker that trails the others.
- **Desktop widgets** &nbsp;`Pro` — status, devices, volume, and presets on your desktop, no app open.

### Now Playing & media
- **Now Playing card** — song, artwork, and play/pause/skip for Spotify or Apple Music, right in the panel.
- **Steps aside for calls & video** &nbsp;`Free` — fades and pauses your music when a call or video plays, then fades back at the same volume.
- **Microphone input card** — pick the input device, adjust its level, or mute it from the panel.

### Bluetooth & sync
- **Reconnects on its own** — a grouped Bluetooth speaker that briefly drops out rejoins when it reconnects, no interruption.
- **Hands back after headphones** — put your AirPods away and Tutti returns to the speaker group and preset you were using.
- **Headphone battery** — shown next to the device name when reported; AirPods get their own icon.
- **Keeps headphones crisp after calls** — uses the built-in mic on calls so your headset doesn't stay stuck at muffled call quality.
- **Stays in sync** — clock-drift correction keeps wired and Bluetooth speakers aligned instead of drifting apart.

### Menu bar, shortcuts & the little things
- **Menu bar quick menu** — device toggles, preset switching, and mute-all without opening the panel.
- **Volume takeover** — keyboard volume keys and the scroll wheel drive the aggregate output globally.
- **Shortcuts, Siri & Spotlight** — switch presets, mute, or set the volume from your automations.
- **Scroll where you point** — hover a device, app, or the mic and the wheel adjusts just that one.
- **Pick your menu bar icon** — classic sound waves or one of ten instruments; the icon fills as volume rises.
- **Sleep timer · gentle fades · Light / Dark / System · launch at login · automatic updates** — the conveniences you'd expect.

### On the way
- **Raycast extension** &nbsp;`Coming soon` — mute, set volume, and switch presets from Raycast.

## Free vs Pro

Every feature above without a tag is **free, forever**. Every new install also gets a **7-day Pro trial** on first launch — no key required. When it ends, all free features keep working without limits.

**Pro unlocks:**

| | |
|---|---|
| **Presets** | one-tap device + volume + per-app combos |
| **Global keyboard shortcuts** | control Tutti from inside any app |
| **Stereo pairing & L/R balance** | split channels across separate speakers |
| **Per-device latency tuning** | align a trailing Bluetooth speaker by ear |
| **Per-app output routing** | send different apps to different speakers |
| **Desktop widgets** | status and control on your desktop |
| **iPhone remote** | control your Mac's audio from your iPhone (free app, needs Pro on the Mac) |

- **$7.99 one-time — no subscription.** All future Pro features included at no extra cost.
- **Up to 2 Macs** per license. Activate and deactivate from Settings › License.
- **14-day refund**, no questions asked — just email support@barrybarrywu.com.

> **Price change:** Tutti Pro moves to **$12.99 on July 22**. Buy before then to lock in **$7.99**. Already own it? You keep every feature, forever — no new charge.

<p align="center">
  <a href="https://checkout.dodopayments.com/buy/pdt_0NfolyiommnaLUYQ5aPqn"><strong>Unlock Tutti Pro — $7.99</strong></a>
</p>

## How Tutti compares

Other great Mac audio tools each solve a piece of this. Here's where Tutti stands.

| | Tutti | Background Music | FineTune | SoundSource | Audio Hijack |
|---|:---:|:---:|:---:|:---:|:---:|
| Same sound to many outputs at once | ✓ | — | ✓ | — | ✓ |
| Per-app volume & EQ | ✓¹ | ✓ | ✓ | ✓ | ✓ |
| Per-app output routing | ✓¹ | — | ✓ | ✓ | ✓ |
| One-tap device presets | ✓ | — | — | — | — |
| **Stereo pairing across devices** | ✓ | — | — | — | — |
| **Per-device Bluetooth latency tuning** | ✓ | — | — | — | — |
| **Now Playing controls** (play / pause / skip) | ✓ | — | — | — | — |
| **iPhone remote** | ✓ | — | — | — | — |
| No virtual driver or system extension | ✓² | — | ✓ | — | — |
| Free to use | ✓ | ✓ | ✓ | — | — |

¹ Per-app features use a native macOS audio tap; requires macOS 14.4 or later.
² Multi-output uses CoreAudio's Aggregate Device and per-app rides the native tap — nothing is installed into your system. Background Music installs a virtual audio device; SoundSource and Audio Hijack install a system extension.

## Use cases

- **Shared listening** — living room speaker and Bluetooth headphones at the same time; play out loud while a friend wears headphones.
- **Streaming & recording** — monitor through headphones while broadcasting to an audience or a capture card.
- **Multi-room playback** — drive wired speakers in the living room and another pair in the bedroom from one Mac.
- **Couch control** — switch presets and pick speakers from your iPhone without getting up.
- **Teaching** — the teacher hears prompts in headphones while the classroom speaker plays for students.

## AirPlay & known limitations

- **AirPlay can't join a group** — macOS won't let AirPlay receivers (HomePod, Apple TV, AirPlay speakers) play in a multi-output group, and only first-party apps can start an AirPlay route. Tutti can use an AirPlay device on its own once macOS has routed to it. See [Roadmap](#roadmap).
- **Per-app features need macOS 14.4+** — per-app volume, Turbo, EQ, and routing rely on the Core Audio process tap added in 14.4. On macOS 13–14.3 everything else works.
- **Bluetooth battery depends on the device** — the level appears only for headsets that report it to macOS.

## Roadmap

- **AirPlay routing inside Tutti** — picking and switching AirPlay receivers straight from the panel, without going to Control Center first. macOS keeps AirPlay discovery on a first-party-only track today; the moment that opens up, Tutti will too.

## Requirements

- macOS 13.0 or later
- Accessibility permission only for the keyboard volume-key takeover (the scroll path doesn't need it)

## Localization

Simplified Chinese · Traditional Chinese · English · Japanese · Korean · French · German · Italian · Spanish.

## Community

News, tips, and behind-the-scenes:

- **Telegram** — [t.me/tuttiapp](https://t.me/tuttiapp)
- **X** — [@BarryBarrywu](https://x.com/BarryBarrywu)

## Source code

As of July 2026, Tutti's source is no longer published. This repository is the home for downloads, releases, the appcast that powers automatic updates, and issue reports. Binaries are distributed under the [EULA](https://tutti.barrybarrywu.com/terms).
