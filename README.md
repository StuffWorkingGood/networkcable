# networkcable# Network Cable & Fiber Optic Reference Tool

A single-file, interactive HTML reference covering every common copper and fiber cable type used in networking — specs, anatomy, connectors, physics, and real-world deployment examples.

## Quick start

Double-click `network_cable_fiber_tool.html`. It opens in any modern browser. No install, no internet, no dependencies.

## What's inside

Eight tabs across the top:

| Tab | Contents |
|---|---|
| **Overview** | Copper vs fiber comparison, end-to-end topology diagram |
| **Copper Cables** | Cat3–Cat8, coax (RG-6/59/11/58, LMR-400), twinax/DAC/AOC, shielding decoded (UTP/FTP/STP/S-FTP), full PoE table (Type 1–4), T568A/B pinout with PoE pair annotations, color cable cross-sections |
| **Fiber Optic** | OM1–OM5, OS1/OS2 with full distance×speed table, SM vs MM ray tracing, total internal reflection diagram, wavelength spectrum (850/1310/1550 nm + O/E/S/C/L bands), loss budget visualization, PC/UPC/APC polish side-view, MTP/MPO pinout, transceiver form factors (SFP through QSFP-DD/OSFP) |
| **Connectors** | SVG illustrations of RJ45, RJ11, BNC, F-type, DAC, LC, SC, ST, FC, MTP/MPO, MT-RJ + color-coding cheat sheet |
| **How They Work** | Differential signaling visual, encoding evolution (Manchester → PAM-16), loss budget math, transceiver naming decoder, latency reality check |
| **Compare** | Drop-down side-by-side comparison of any two cables |
| **Use-Case Picker** | Pick distance + speed + EMI + PoE → get a cable recommendation |
| **Real Examples** | Six full deployment scenarios with topology diagrams and bills of materials: home FTTH, mid-size office floor, data center top-of-rack, industrial plant floor, campus inter-building, and low-latency / HFT rack |
| **Quick Reference** | Standards bodies, ISO Class ↔ Cat mapping, bend radii, testing gear, common gotchas |

## Features

- **Interactive comparison engine** — pick any two cables, see specs aligned
- **Use-case picker** — describe your scenario, get a recommendation with rationale
- **Filter search** on the copper table
- **17+ custom SVG diagrams** including cable cross-sections, fiber ray tracing, wavelength charts, polish angles, network topologies
- **Color-accurate pinouts** matching T568A/B wire colors
- **Real bills of materials** with actual switch/optic part-name examples

## Tech notes

- Pure HTML/CSS/JS, single file, ~85 KB
- No external CDNs, no fonts, no images — every diagram is inline SVG
- Works offline, on any device, in any modern browser
- Dark theme; mobile-responsive grid

## File structure

```
outputs/
├── network_cable_fiber_tool.html    # The tool itself
└── README.md                        # This file
```

## Customizing

Open `network_cable_fiber_tool.html` in any text editor:

- **Add a cable type** → append to the `cables` array near the bottom of the `<script>` block. It auto-populates the Compare dropdowns.
- **Tweak picker logic** → edit the `recommend()` function in the same script.
- **Change colors** → CSS variables at the top of the `<style>` block (`--copper`, `--fiber`, `--accent`, etc.).
- **Add a new tab** → add a `<button class="tab-btn" data-tab="newid">` to the nav and a `<section id="newid">` to the main body.

## Coverage caveats

This tool reflects current standards as of 2026. A few things deliberately not covered in depth:

- Pre-Ethernet copper (Token Ring, ARCnet)
- Plastic optical fiber (POF) and HDMI-over-fiber consumer gear
- Sub-1G specialty industrial buses (Foundation Fieldbus, HART, AS-i)
- Subsea / submarine cable engineering

For those, treat this tool as a starting point and pair it with vendor specifications.