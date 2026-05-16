---
date: 2026-05-16
status: approved
---

# D4rk-Wolf GitHub Profile README — Design Spec

## Goal

Redesign `profile/README.md` to read as a professional studio profile: serious and active, technically credible, and brand/product-forward — all within the first scroll. No personal names; everything under the D4rk-Wolf studio identity.

## Structure

### 1. Header

- H1: `D4rk-Wolf`
- One-line positioning statement: `Independent software studio — Android · Dev Tools · Embedded Systems · Web3`
- Location and founding: `Manchester, UK · Est. 2023`
- Inline social badges (shields.io, flat style): Website · Twitter/X · Discord

### 2. Projects Table (Hero Section)

Dominant section. HTML table, one row per project. Each row contains:

| Column | Content |
| --- | --- |
| Name | Linked to repo or product URL |
| Platform | Badge: `Android` / `Desktop` / `Hardware` / `Web` / `Web3` |
| Status | Badge: `Shipping` / `In Development` / `Prototype` / `Internal` |
| Description | One-line summary |
| Tech | Mini shields.io badges for primary stack |

**Projects to include:**

| Project | Platform | Status | Description | Tech |
| --- | --- | --- | --- | --- |
| DoseFlow | Android | Shipping | Medication tracking | Kotlin, Compose |
| AutoVibe | Android | Shipping | Atmosphere automation | Kotlin, Compose |
| GarageGuardian | Hardware | Shipping | IoT garage monitoring | Kotlin, ESP32 |
| JounoApp | Android | Shipping | Markdown journaling | Kotlin, Compose |
| AI Document Templates | Desktop | Shipping | AI doc tooling for devs | React, Tauri |
| Smart Helmet | Hardware | Prototype | Cyclist safety hardware | ESP32 |
| Nexus | Web3 | In Development | Web3 social platform | — |
| Sovereign OS | Systems | Internal | Custom Linux platform | Linux |

### 3. Stats + Tech Stack (Side by Side)

Two-column HTML table:

- **Left:** GitHub stats card + streak counter via `github-readme-stats` (anuraghazra). Dark theme.
- **Right:** Tech stack badges grouped into three rows:
  - `Mobile`: Kotlin · Jetpack Compose · Android
  - `Desktop/Web`: React · Tauri · TypeScript
  - `Systems`: ESP32 · Linux · C++

All badges: shields.io, flat style, consistent colour scheme.

### 4. Philosophy (Closing)

Single blockquote, no header:

> Small teams. Real products. On-device data. No hype.

## Style Decisions

- No personal names anywhere
- Pure studio brand voice throughout
- shields.io badges: flat style, dark-compatible colours
- GitHub stats: dark theme to match brand
- No emoji unless they serve a functional purpose (platform icons)
- No mission statements, no padding copy

## Out of Scope

- Custom banner image or logo (not available)
- Animated elements
- LinkedIn (excluded by request)
