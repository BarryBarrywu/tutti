<p align="right">English · <a href="README.zh.md">中文</a></p>

<p align="center">
  <img src="assets/readme/hero-en.svg" width="100%" alt="Tutti: Bring your setup together. Sound and display control for Mac.">
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/BarryBarrywu/tutti?style=flat-square&color=blue&label=release" alt="Release">
  <img src="https://img.shields.io/badge/macOS-13.0+-000000?style=flat-square&logo=apple&logoColor=white" alt="macOS 13+">
  <img src="https://img.shields.io/github/downloads/BarryBarrywu/tutti/total?style=flat-square&color=orange&label=downloads" alt="Downloads">
  <img src="https://img.shields.io/badge/Pro-$12.99_one--time-38bdf8?style=flat-square" alt="Pro $12.99 one-time">
</p>

<p align="center">
  <img src="docs/screenshots/panel.webp" alt="Tutti menu bar panel in light and dark" width="720">
</p>

<p align="center"><sub><strong>No virtual driver · no system extension · no telemetry · no account.</strong> Notarized by Apple. Quit Tutti and your audio setup is exactly as it was.</sub></p>

## One panel for sound and screens

An external display is often both another screen and another audio output, but macOS keeps brightness and sound in separate places. Tutti brings audio outputs, every app, displays, and presets into one menu bar panel.

Play through several devices at once, adjust each device and app, control brightness for one display or a whole group, then save the complete setup as a preset. Tutti uses Apple’s own frameworks, with no virtual audio driver or system extension to install.

- **One sound, every speaker**: play through speakers, headphones, and display audio together.
- **Every app, its own settings**: control volume, EQ, and output separately.
- **Every display, the right brightness**: control one display or a group, with external displays following the built-in screen.
- **Your whole setup, one preset**: restore outputs, volume, apps, and display brightness together.

## Install

Download the [latest DMG](https://github.com/BarryBarrywu/tutti/releases/latest/download/Tutti.dmg), or install with Homebrew:

```bash
brew install --cask barrybarrywu/tap/tutti
```

Tutti checks for updates automatically after installation.

## Tutti Remote — now on the App Store

Control Mac outputs, device and app volume, music playback, and display brightness from your iPhone. The Mac remains in charge; Tutti Remote simply puts the whole panel within reach. Pairs over your local network. The iPhone app is free; controlling your Mac requires Tutti Pro on the Mac.

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
- **Detailed group HUDs** — volume and brightness feedback shows every selected output or display and its resulting level, not just the group average.
- **Per-device adjustment steps** — give sensitive displays and wide-range speakers their own step sizes while anything else follows the default.
- **Three-state status** — playing on all, partially muted, or all muted, with a matching color dot.
- **Hot-swap without a gap** — add or remove a speaker mid-playback without cutting the sound.
- **Device Guard** — set a priority order for your outputs and lock the default output, input, and volume; when macOS or another app switches them behind your back, Tutti puts them back.
- **Remembers your setup** — your speaker group, per-device volumes, and mute survive quitting Tutti and app updates.

### Display control &nbsp;`macOS 15+`
- **Group + per-display brightness** — select the displays you want, then adjust the whole brightness group or one screen at a time.
- **Hardware control where supported** — built-in and compatible Apple displays use system brightness, DDC/CI displays use hardware controls, and other displays can use clearly identified Software Dimming.
- **Follow the built-in display** — external displays can keep their brightness offset while following manual changes and macOS automatic brightness.
- **Brightness keys & scrolling** — the keyboard brightness keys control the selected displays with Tutti's progress HUD; hover and scroll to adjust a group or one display.
- **Display presets + iPhone control** &nbsp;`Pro` — save display selection and brightness in presets, or control them from Tutti Remote 1.1.0.
- **Brightness Upscaling (v1.10.0)** &nbsp;`Pro` — use available EDR headroom to move a compatible XDR display's own slider above 100%, with Gamma or Metal. Presets can save and restore each display's switch and level. [Compatibility and setup](https://tutti.barrybarrywu.com/docs/#upscaling).

Upscaling can affect HDR content and color accuracy; it does not detect HDR or turn itself off automatically. Group controls, brightness keys, direct brightness shortcuts, Remote, automation, Brightness Following, and scrolling remain within 100%. Standard Studio Display and generic third-party HDR displays are excluded; the linked guide distinguishes software compatibility from hardware testing.

Tutti's display brightness engine builds on the open-source [Crisp](https://github.com/didriksg/Crisp) project. Thanks to didriksg and its contributors for sharing their work.

### Per-app audio control &nbsp;`macOS 14.4+`
- **Per-app volume & Turbo** &nbsp;`Free` — give each app its own level; Turbo adds a 2× boost. Driver-free, via a native audio tap.
- **Per-app equalizer** &nbsp;`Free` — a draggable 6-band EQ curve for any app, or a built-in preset.
- **Per-app output** &nbsp;`Pro` — send different apps to different speakers; keep a call on the laptop while music fills the room.
- **See where sound goes** — output devices show small badges of the apps routed to them.
- **Ignore apps you don't manage** — right-click any app to tuck it out of the list.

<p align="center">
  <img src="docs/screenshots/mac-per-app-eq.webp" alt="Per-app equalizer curve" width="320">
</p>

### Pro power tools
- **Presets** &nbsp;`Pro` — save device + volume + per-app combos and switch with one click; each gets its own emoji.
- **Global keyboard shortcuts** &nbsp;`Pro` — hotkeys to open the panel, mute, switch preset, or nudge an app's volume from inside any app.
- **Stereo pairing across devices** &nbsp;`Pro` — send the left channel to one speaker and the right to another — two speakers, one stereo pair.
- **Per-speaker left-right balance** &nbsp;`Pro` — lean any speaker's sound toward one side when it sits off-center.
- **Per-device latency tuning** &nbsp;`Pro` — add delay to faster outputs to align them with a slower speaker; it cannot make Bluetooth audio arrive sooner.
- **Desktop widgets** &nbsp;`Pro` — status, devices, volume, and presets on your desktop, no app open.

<p align="center">
  <img src="docs/screenshots/mac-stereo-split.webp" alt="Stereo pairing across devices" width="320">
  &nbsp;&nbsp;
  <img src="docs/screenshots/mac-latency-balance.webp" alt="Per-device latency and balance" width="320">
</p>

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
- **Independent panel layouts** — Outputs, Apps, Input, and Displays can each follow the popup size or stay fixed to one or two rows.
- **Pick your menu bar icon** — classic sound waves or one of ten instruments; the icon fills as volume rises.
- **Sleep timer · gentle fades · Light / Dark / System · launch at login · automatic updates** — the conveniences you'd expect.

### More ways to control
- **Raycast extension** — mute, set volume, and switch presets from Raycast.

  <a href="https://www.raycast.com/Barrybarrywu/tutti" title="Install Tutti Raycast Extension"><img src="https://www.raycast.com/Barrybarrywu/tutti/install_button@2x.png?v=1.1" height="64" style="height: 64px;" alt="Install Tutti on Raycast" /></a>

## Free vs Pro

Every feature above without a tag is **free, forever**. Every new install also gets a **7-day Pro trial** on first launch — no key required. When it ends, all free features keep working without limits.

**Pro unlocks:**

| | |
|---|---|
| **Presets** | one-tap device + volume + per-app combos |
| **Global keyboard shortcuts** | control Tutti from inside any app |
| **Stereo pairing & L/R balance** | split channels across separate speakers |
| **Per-device latency tuning** | delay faster outputs to match a slower speaker |
| **Per-app output routing** | send different apps to different speakers |
| **Desktop widgets** | status and control on your desktop |
| **Raycast control** | control Tutti from Raycast — mute, set volume, or apply presets |
| **iPhone remote** | control your Mac's audio from your iPhone (free app, needs Pro on the Mac) |
| **Display presets & iPhone brightness control** | save display groups and brightness, then control them from your iPhone |
| **Brightness Upscaling (v1.10.0)** | above-100% brightness on compatible XDR displays, including saved preset scenes |

- **$12.99 one-time — no subscription.** All future Pro features included at no extra cost.
- **One Mac at a time** per license. Activate and deactivate from Settings › License.
- **14-day refund**, no questions asked — just email support@barrybarrywu.com.

<p align="center">
  <a href="https://checkout.dodopayments.com/buy/pdt_0NfolyiommnaLUYQ5aPqn"><strong>Unlock Tutti Pro — $12.99</strong></a>
</p>

## How Tutti compares

Other great Mac audio tools each solve a piece of this. Here's where Tutti stands.

| | Tutti | Background Music | FineTune | SoundSource | Audio Hijack |
|---|:---:|:---:|:---:|:---:|:---:|
| Same sound to many outputs at once | ✓ | — | ✓ | ✓ | ✓⁴ |
| Per-app volume | ✓¹ | ✓ | ✓ | ✓ | ✓⁴ |
| Per-app EQ | ✓¹ | — | ✓ | ✓ | ✓⁴ |
| Third-party Audio Unit effects | — | — | — | ✓ | ✓ |
| Per-app output routing | ✓¹ | — | ✓ | ✓ | ✓ |
| One-tap device + app presets | ✓ | — | — | ✓ | — |
| Preferred device order | ✓ | — | ✓ | ✓ | — |
| AirPlay in a multi-output group | — | — | — | ✓ | — |
| **Stereo pairing across devices** | ✓ | — | — | — | — |
| **Per-device Bluetooth latency tuning** | ✓ | — | — | — | — |
| **Now Playing controls** (play / pause / skip) | ✓ | — | — | — | — |
| **iPhone remote** | ✓ | — | — | — | — |
| No additional audio component to install | ✓² | — | ✓ | — | ✓³ |
| Free, unlimited use | ✓ | ✓ | ✓ | — | — |

¹ Per-app features use a native macOS audio tap; requires macOS 14.4 or later.

² Tutti's multi-output uses a CoreAudio Aggregate Device and per-app control uses the native tap — nothing extra is installed. Background Music installs a virtual audio device; SoundSource requires its ARK plugin.

³ On macOS 14.4 or later, Audio Hijack uses native system audio access without installing an additional audio component.

⁴ Audio Hijack provides these capabilities through configurable sessions rather than a menu-bar mixer.

Competitor capabilities checked against the current documentation for [Background Music](https://github.com/kyleneideck/BackgroundMusic), [FineTune](https://github.com/ronitsingh10/FineTune), [SoundSource 6](https://www.rogueamoeba.com/soundsource/whatsnew.php), and [Audio Hijack](https://rogueamoeba.com/support/manuals/audiohijack/).

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
- Accessibility permission only for keyboard volume- and brightness-key takeover (the scroll path doesn't need it)

## Localization

Simplified Chinese · Traditional Chinese · English · Japanese · Korean · French · German · Italian · Spanish.

## Community

News, tips, and behind-the-scenes:

- **Telegram** — [t.me/tuttiapp](https://t.me/tuttiapp)
- **X** — [@BarryBarrywu](https://x.com/BarryBarrywu)

## Source code

As of July 2026, Tutti's source is no longer published. This repository is the home for downloads, releases, the appcast that powers automatic updates, and issue reports. Binaries are distributed under the [EULA](https://tutti.barrybarrywu.com/terms).
