# POWERTOP

![license](https://img.shields.io/badge/license-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-laptops-lightgrey)

> Anticloud-hardened packaging of the upstream project `POWERTOP` in category **LAPTOPS**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** LAPTOPS · **Upstream:** https://github.com/kDolphin/PowerTop · **Upstream pin:** `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# PowerTop

**English** | **[简体中文](README.zh-CN.md)**

A clean, lightweight menu bar app that shows you exactly how much power your MacBook is using.

<p align="center">
  <img src="https://img.shields.io/badge/version-1.4.2-blue" />
  <img src="https://img.shields.io/badge/platform-macOS%2014%2B-blue" />
  <img src="https://img.shields.io/badge/architecture-Apple%20Silicon-green" />
  <img src="https://img.shields.io/badge/license-MIT-orange" />
</p>

> **MacBook only** — Requires a Mac with a built-in battery (Apple Silicon MacBook).

## Finally Know How Much Power You're Using

macOS never tells you the actual watts your MacBook is consuming right now. PowerTop changes that.

It gives you clear, real-time power information directly in the menu bar and a simple popover — so you can see exactly what's happening with power on your machine.

## Key Features

- **Optional menu bar wattage** — Show live power like `23W` right in the menu bar when you want it.
- **Power flow diagram** — See at a glance whether power is coming from the charger, the battery, or both at the same time.
- **Instant power numbers** — System power, charger output, and battery charge or discharge rate.
- **Charger load** — Know your adapter's wattage and how much of it is being used.
- **Battery overview** — Quick view of battery level, health, temperature, and cycle count.
- **Estimated battery time** — Time to empty or full in the popover and detail view; respects macOS charge limits (80/85/90/95%) and third-party apps like AlDente.
- **Detailed information** — Auto-detected cell topology (e.g. 3S2P), series-group voltage, parallel cell currents, charging status, and lifetime stats.

Everything updates live and stays accurate even when you plug in or unplug your charger.

## Why People Use PowerTop

- Curious about real power consumption on their MacBook
- Want to know if their charger is powerful enough during heavy work
- Like seeing when the battery is helping supply power
- Want a simple, beautiful way to monitor battery health and charging behavior

It's a small, native app that does one thing well — no bloat, no subscriptions.

## Installation

### Download (Recommended)

Download the latest `PowerTop.zip` from the [Releases](https://github.com/kDolphin/PowerTop/releases) page:

1. Unzip the file
2. Drag `PowerTop.app` into your `/Applications` folder
3. First launch: right-click the app → **Open** (the app is not signed)

### Build from Source

```bash
git source https://github.com/kDolphin/PowerTop.git
cd PowerTop
bash build.sh
open build/PowerTop.app
```

## Requirements

- Apple Silicon MacBook (M-series)
- macOS 14 (Sonoma) or later

## How to Use

1. Open PowerTop — the icon appears in your menu bar.
2. Click the icon to open the popover with the power flow diagram and current readings.
3. Turn on **Show Power in Menu Bar** at the bottom if you want the wattage always visible.
4. Click **Details** for a full breakdown of power and battery information.

## Screenshots

### Popover

| **AC Powered** | **Battery Discharging** |
|----------------|--------------------------|
| <a href="screenshot/popover-ac-powered.png" target="_blank"><img src="screenshot/popover-ac-powered.png" width="260" alt="AC Powered"></a> | <a href="screenshot/popover-battery-discharging.png" target="_blank"><img src="screenshot/popover-battery-discharging.png" width="260" alt="Battery Discharging"></a> |

| **AC Charging** | **AC + Battery Supplement** |
|-----------------|------------------------------|
| <a href="screenshot/popover-ac-charging.png" target="_blank"><img src="screenshot/popover-ac-charging.png" width="260" alt="AC Charging"></a> | <a href="screenshot/popover-ac-supplement.png" target="_blank"><img src="screenshot/popover-ac-supplement.png" width="260" alt="AC + Battery Supplement"></a> |

### Detail Window

| **Power & Battery Health** | **Cell Data** |
|----------------------------|---------------|
| <a href="screenshot/detail-window-health.png" target="_blank"><img src="screenshot/detail-window-health.png" width="400" alt="Power and battery health"></a> | <a href="screenshot/detail-window-cells.png" target="_blank"><img src="screenshot/detail-window-cells.png" width="400" alt="Cell topology and balance"></a> |

## What's New

### v1.4.2

- **Popover dismiss** — Clicking outside the panel closes it on macOS 15/26 as well (status-item popovers in menu-bar apps often miss system `.transient` dismiss; issue #13)

### v1.4.1

- **Menu bar label** — Use the native status item title so wattage no longer jumps after the first refresh or stay emphasized when switching displays

### v1.4.0

- **System popover** — Menu bar panel uses a standard `NSPopover` (corners, material, and size follow the system). Fixes background/corner glitches when content height changes.

### v1.3.9

- **Supplement time-to-empty** — When estimating battery time during AC + battery supplement, use pack outflow only, not full system load (thanks @Collinw24, issue #12)

### v1.3.8

- **Manufacture date** — Read explicit `ManufactureDate` from the pack (`YYYY-MM-DD`); stop treating `ManufacturerData` as a week code (thanks @Collinw24, PR #10 / issue #7)

### v1.3.7

- **AC power-gap classification** — When system load exceeds AC input, only treat the battery as discharging if amperage or BatteryPower shows discharge; do not invent supplement power from the load gap alone (reduces false “battery supplement” during telemetry lag; issue #8)

### v1.3.6

- **Manufacture date parsing** — Prefer length-prefixed fields in `ManufacturerData` and reject far-future week codes (avoids bogus dates such as 2035-W14 on some machines; issue #7)

### v1.3.5

- **Popover type consistency** — Battery level and health rows use the same 12pt system font as other metric rows (no shrink-to-fit, no rounded digits)

### v1.3.4

- **Aligned metric bars** — Popover battery level/health rows use a fixed label column and icons so progress bars line up in both Chinese and English

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Unknown (no standard manifest detected)** (manifests: none detected; scanned in UPSTREAM_CLONE)
- Top-level source layout: `PowerTop/`, `screenshot/`, `scripts/`
- Snapshot size: **42 files**, **3649 lines of code** (measured; see Benchmarks)
- Primary languages: `.png` (16), `.swift` (14), `.json` (3), `(none)` (2), `.md` (2), `.sh` (2)
- Upstream commit pinned for this packaging: `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`

---

## Installation

No installation section was found in the upstream readme, so the commands below are generated from the manifests detected in this project directory.

```sh
# No standard manifest detected. Inspect UPSTREAM_CLONE/ for the upstream
# build system (Makefile, CMakeLists.txt, configure, ...) and follow it.
```

Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

- Curious about real power consumption on their MacBook
- Want to know if their charger is powerful enough during heavy work
- Like seeing when the battery is helping supply power
- Want a simple, beautiful way to monitor battery health and charging behavior

It's a small, native app that does one thing well — no bloat, no subscriptions.

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

The upstream API surface is defined by the `POWERTOP` source tree vendored in `UPSTREAM_CLONE/` (Unknown (no standard manifest detected) ecosystem). Public entry points:

- Source modules: `PowerTop/`, `screenshot/`, `scripts/`
- Overlay API: `anticloud/cli.py` exposes 13 subcommands with JSON stdout; `anticloud/bench/runner.py` runs the 16-check suite; `anticloud/provenance/chain.py` exposes the SHA3-256 + Ed25519 provenance chain.

---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Unknown (no standard manifest detected) |
| Manifests detected | none |
| Files in snapshot | 42 |
| Lines of code | 3649 |
| Dependency references | 0 |
| Upstream license | MIT |
| Overlay license | Anticommons 0.1.0 |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

- **Smarter limit detection** — Ignores stale AlDente configs when `useTahoeNativeLimit` is enabled; only uses Optimized Charging `DailyMaxSoc` when the pause flag is active

*Section quoted from the upstream readme.*
Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `POWERTOP` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: MIT** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
MIT License

Copyright (c) 2025 kdolphin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original MIT terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `MIT` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `POWERTOP` (category: LAPTOPS)
- **Upstream URL:** https://github.com/kDolphin/PowerTop
- **Pinned commit (SHA):** `fc38769ba42c3fa3b397dcd1b7116d2aa2f68424`
- **Branch:** main
- **Pin provenance:** GitHub API commits/main. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`696d05304028adbb37da33b2703fd072cccdcc1a9ac457708a2188b2ff7d3fa1`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

