<div align="center">

<br/>

<img src="assets/icon.png" width="140" alt="XiaoArk"/>

<br/><br/>

# XiaoArk · 小方舟

**A tiny boat, sailing across the vast sea.**

[![Release](https://img.shields.io/github/v/release/Shamnick/XiaoArk?style=flat-square&color=0A7EA4&label=release)](https://github.com/Shamnick/XiaoArk/releases)
[![Platform](https://img.shields.io/badge/platform-macOS%20·%20Windows%20·%20Linux%20·%20Android-30D5C8?style=flat-square)](https://github.com/Shamnick/XiaoArk/releases)
[![License](https://img.shields.io/badge/license-open%20source-1B4F72?style=flat-square)](LICENSE)

*A clean, fast and free network proxy client — designed & maintained by xiaoxiao*

**[简体中文](README.md)** · **English**

</div>

---

## 🌊 Why XiaoArk

The ocean of information is boundless, yet not every little boat can sail freely.

**XiaoArk** is built for exactly that: named after the sea, shaped like a sail. The gradient on its icon — from turquoise shallows to deep sea blue — is a journey from the coast to the open ocean. The raised sail is speed; the dot beneath it is your coordinate, reminding you that you always know where you're going.

It is not bloated, not noisy. Open it, set your course, then forget it exists — until you arrive at any shore you wish.

## ✨ Features

### 🚀 Full Protocol Support

One subscription, every mainstream protocol covered:

`VMess` · `VLESS` · `Trojan` · `Shadowsocks` · `ShadowsocksR` · `Hysteria / Hysteria2` · `TUIC` · `WireGuard` · `Socks5` · `HTTP`

### 🧭 Smart Routing

- **Rule-based routing**: auto-switch by domain, IP or region — direct at home, proxied abroad
- **TUN global mode**: captures all system traffic, even protocols apps don't support natively
- **Proxy group policies**: manual selection, auto latency-test, load balancing — your call
- **Real-time latency testing**: the true speed of every node, at a glance

### 🔗 Subscription Management

- One-click import via `xiaoark://` and `clash://` links
- Multiple subscriptions side by side, auto-updated on schedule
- QR-code scan import (mobile)

### 🎨 Modern Experience

- Fluent Flutter UI with light/dark themes following the system
- Menu-bar tray states: **sail up = connected, sail down = disconnected**
- Connection details, traffic statistics, log viewer — painless debugging
- WebDAV cloud backup: sync configs anywhere, zero cost to switch devices

### 🛡 Independent & Clean

- Independent Bundle ID and config directory — coexists peacefully with any similar app
- No ads, no tracking, no bundling
- Open source and transparent — every line auditable

## 📸 Screenshots

<div align="center">

<img src="assets/screenshots/dashboard.png" width="760" alt="XiaoArk Dashboard"/>

**Dashboard** · real-time traffic, node latency and connection stats in one view

<br/>

<img src="assets/screenshots/tray_states.png" width="560" alt="Tray States"/>

**Menu-bar Tray** · sail up means connected, sail down means disconnected — no need to open the window

<br/>

<img src="assets/screenshots/dmg_install.png" width="560" alt="Installer"/>

**Installer** · ocean-themed DMG — it looks like our own from the very first glance

</div>

## ⬇️ Download

Get the latest version from [**Releases**](https://github.com/Shamnick/XiaoArk/releases):

| Platform | Architecture | File |
|---|---|---|
| macOS | Apple Silicon (M series) | `XiaoArk-*-macos-arm64.dmg` |
| macOS | Intel | `XiaoArk-*-macos-amd64.dmg` |

### Install

1. Open the downloaded `.dmg`
2. Drag **XiaoArk.app** into **Applications**
3. If macOS warns on first launch: **System Settings → Privacy & Security → Open Anyway**

## 🚀 Quick Start

```text
① Get a subscription link   → copy the subscription URL from your provider
② Import into XiaoArk       → Profiles page → New → paste the link → Save
③ Pick a node               → Proxies page → choose the node with lowest latency
④ Set sail                  → flip the switch on the home page — sail up, online
```

## 🎨 Design Guidelines

| Element | Spec |
|---|---|
| Chinese name | 小方舟 |
| English name | XiaoArk |
| Primary color | ![#30D5C8](https://img.shields.io/badge/-%2330D5C8-30D5C8?style=flat-square) Turquoise `#30D5C8` |
| Secondary color | ![#1B4F72](https://img.shields.io/badge/-%231B4F72-1B4F72?style=flat-square) Deep Sea Blue `#1B4F72` |
| Icon | white rounded square · one sail, one dot · ocean gradient |
| Philosophy | minimal, far-sailing, reliable |

## 🏗 Architecture

```text
┌─────────────────────────────────────────┐
│        XiaoArk desktop / mobile app      │  Flutter · Dart
├─────────────────────────────────────────┤
│        Rust service bridge               │  rust_api · helper
├─────────────────────────────────────────┤
│        Clash Meta (mihomo) core          │  Go · rule engine · TUN
└─────────────────────────────────────────┘
```

- **UI layer**: Flutter cross-platform rendering — designed once, consistent everywhere
- **Bridge layer**: high-performance service channel in Rust, handling process & privilege management
- **Core layer**: the battle-tested Clash Meta proxy engine
- **Release**: built in the cloud with GitHub Actions — push a tag, get a release

## 🗺 Roadmap

- [x] macOS Apple Silicon native build
- [ ] Full ocean-themed UI
- [ ] First-launch onboarding
- [ ] Windows / Linux / Android cloud builds
- [ ] Chinese as the default UI language

## ❓ FAQ

<details>
<summary><b>macOS says the app is "damaged and can't be opened"?</b></summary>

This is the standard warning for unsigned apps. Run in Terminal:

```bash
xattr -dr com.apple.quarantine /Applications/XiaoArk.app
```

</details>

<details>
<summary><b>Subscription link doesn't respond when clicked?</b></summary>

Make sure it starts with `xiaoark://` or `clash://`, or paste it manually inside the app.

</details>

<details>
<summary><b>Can't enable TUN mode?</b></summary>

TUN requires a system service. Authorize it once when prompted in Settings — it works automatically afterwards.

</details>

## 🙏 Credits

This project is a derivative work based on [FlClash](https://github.com/chen08209/FlClash) (GPL-3.0). Huge thanks to the original author and the [mihomo](https://github.com/MetaCubeX/mihomo) core community. All changes made by XiaoArk are publicly auditable in this repository.

---

<div align="center">

<br/>

**XiaoArk · 小方舟**

Made with 🌊 by xiaoxiao

<br/>

</div>
