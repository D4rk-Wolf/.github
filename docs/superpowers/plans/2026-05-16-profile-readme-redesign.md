# D4rk-Wolf Profile README Redesign — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Rewrite `profile/README.md` to be a professional studio profile for D4rk-Wolf with header, projects hero table, stats/tech stack, and closing philosophy.

**Architecture:** Single-file rewrite of `profile/README.md`. Each task appends a new section to the file in order. The stats section uses an HTML table for two-column layout since GitHub Markdown has no native multi-column support; all other sections use standard Markdown. Badge images served by shields.io; GitHub stats by github-readme-stats (anuraghazra) and streak-stats (demolab).

**Tech Stack:** GitHub Markdown, shields.io, github-readme-stats (anuraghazra), streak-stats (demolab)

---

## File Map

| File | Action |
| --- | --- |
| `profile/README.md` | Full rewrite |
| `docs/superpowers/specs/2026-05-16-profile-readme-design.md` | Committed alongside (already written) |

---

### Task 1: Header

**Files:**
- Modify: `profile/README.md` — overwrite entire file with header

- [ ] **Step 1: Overwrite README with header**

Replace the entire contents of `profile/README.md` with:

```markdown
# D4rk-Wolf

Independent software studio — Android · Dev Tools · Embedded Systems · Web3  
Manchester, UK · Est. 2023

[![Website](https://img.shields.io/badge/Website-d4rkwolf.co.uk-000000?style=flat&logo=googlechrome&logoColor=white)](https://d4rkwolf.co.uk/)
[![Twitter](https://img.shields.io/badge/Twitter-%40turkishDW-000000?style=flat&logo=x&logoColor=white)](https://twitter.com/turkishDW)
[![Discord](https://img.shields.io/badge/Discord-Join-000000?style=flat&logo=discord&logoColor=white)](https://discord.gg/DRwwWJ7m)
```

- [ ] **Step 2: Verify header renders**

Open `profile/README.md` in VS Code markdown preview (Ctrl+Shift+V). Confirm:
- Studio name renders as H1
- Positioning line and location render beneath it
- Three badges appear with correct labels and correct destination URLs

---

### Task 2: Projects Hero Table

**Files:**
- Modify: `profile/README.md` — append projects section

- [ ] **Step 1: Append projects table**

Add the following immediately after the header block:

```markdown

---

## Projects

| Project | Platform | Status | Description | Tech |
| --- | --- | --- | --- | --- |
| [DoseFlow](https://github.com/D4rk-Wolf/DoseFlow) | ![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white) | ![Shipping](https://img.shields.io/badge/Shipping-brightgreen?style=flat) | Medication tracking for Android | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white) ![Compose](https://img.shields.io/badge/Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white) |
| [AutoVibe](https://github.com/D4rk-Wolf/AutoVibe) | ![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white) | ![Shipping](https://img.shields.io/badge/Shipping-brightgreen?style=flat) | Atmosphere automation for Android | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white) ![Compose](https://img.shields.io/badge/Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white) |
| [GarageGuardian](https://github.com/D4rk-Wolf/GarageGuardian) | ![Hardware](https://img.shields.io/badge/Hardware-E7352C?style=flat&logo=espressif&logoColor=white) | ![Shipping](https://img.shields.io/badge/Shipping-brightgreen?style=flat) | IoT garage monitoring with Android + ESP32 | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white) ![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat&logo=espressif&logoColor=white) |
| [JounoApp](https://github.com/D4rk-Wolf/JounoApp) | ![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white) | ![Shipping](https://img.shields.io/badge/Shipping-brightgreen?style=flat) | Markdown journaling for Android | ![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white) ![Compose](https://img.shields.io/badge/Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white) |
| [AI Document Templates](https://github.com/D4rk-Wolf/ai-document-templates) | ![Desktop](https://img.shields.io/badge/Desktop-0078D4?style=flat&logo=tauri&logoColor=white) | ![Shipping](https://img.shields.io/badge/Shipping-brightgreen?style=flat) | AI doc tooling for developers | ![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black) ![Tauri](https://img.shields.io/badge/Tauri-24C8D8?style=flat&logo=tauri&logoColor=white) |
| Smart Helmet | ![Hardware](https://img.shields.io/badge/Hardware-E7352C?style=flat&logo=espressif&logoColor=white) | ![Prototype](https://img.shields.io/badge/Prototype-orange?style=flat) | Cyclist safety hardware prototype | ![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat&logo=espressif&logoColor=white) |
| Nexus | ![Web3](https://img.shields.io/badge/Web3-627EEA?style=flat&logo=ethereum&logoColor=white) | ![In Development](https://img.shields.io/badge/In%20Development-blue?style=flat) | Web3 social platform | |
| Sovereign OS | ![Systems](https://img.shields.io/badge/Systems-FCC624?style=flat&logo=linux&logoColor=black) | ![Internal](https://img.shields.io/badge/Internal-lightgrey?style=flat) | Custom Linux platform | ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black) |
```

> **Project links:** DoseFlow, AutoVibe, GarageGuardian, JounoApp, and AI Document Templates use assumed GitHub repo names. Before committing, verify each link resolves. Smart Helmet, Nexus, and Sovereign OS are intentionally unlinked (prototype / unreleased / internal). If a repo name differs from the assumed name, update the link in the table.

- [ ] **Step 2: Verify table renders**

Check markdown preview. Confirm:
- All 8 projects appear as rows
- Platform, Status, and Tech columns render as coloured badges
- No badge image is broken (no alt-text-only placeholders)
- Table is readable without horizontal scrolling at standard viewport

---

### Task 3: Stats + Tech Stack (Two-Column)

**Files:**
- Modify: `profile/README.md` — append stats section

- [ ] **Step 1: Append two-column stats and tech section**

Add the following immediately after the projects table:

```markdown

---

<table>
<tr>
<td width="55%" valign="top">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=D4rk-Wolf&show_icons=true&theme=github_dark&hide_border=true&count_private=true)

![GitHub Streak](https://streak-stats.demolab.com/?user=D4rk-Wolf&theme=github-dark&hide_border=true)

</td>
<td width="45%" valign="top">

**Mobile**  
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat&logo=jetpackcompose&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=flat&logo=android&logoColor=white)

**Desktop / Web**  
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Tauri](https://img.shields.io/badge/Tauri-24C8D8?style=flat&logo=tauri&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)

**Systems**  
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat&logo=espressif&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat&logo=linux&logoColor=black)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)

</td>
</tr>
</table>
```

> **Stats cards:** Both widgets use `D4rk-Wolf` as the username. If D4rk-Wolf is a GitHub organisation rather than a personal account, the streak widget will likely fail to render — remove it and keep only the stats card. The stats card (`github-readme-stats`) supports orgs via the `username` param.

- [ ] **Step 2: Verify two-column layout**

Check markdown preview or push to GitHub. Confirm:
- Stats card renders on the left with dark theme
- Streak card renders below stats on the left (or is absent if org account)
- Tech stack badges render on the right under three bold group headings
- Layout is visually two-column, not stacked

---

### Task 4: Philosophy + Final Commit

**Files:**
- Modify: `profile/README.md` — append closing line

- [ ] **Step 1: Append closing philosophy blockquote**

Add the following at the very end of the file:

```markdown

---

> Small teams. Real products. On-device data. No hype.
```

- [ ] **Step 2: Verify full README end-to-end**

Open in markdown preview or push to GitHub. Scroll through and confirm:
- No content from the old README remains
- Four sections flow in order: header → projects → stats/tech → philosophy
- No broken badge images anywhere
- Social badge links open correct URLs (d4rkwolf.co.uk, twitter.com/turkishDW, discord.gg/DRwwWJ7m)
- No personal name appears anywhere in the rendered output

- [ ] **Step 3: Commit**

```bash
git add profile/README.md docs/superpowers/specs/2026-05-16-profile-readme-design.md docs/superpowers/plans/2026-05-16-profile-readme-redesign.md
git commit -m "redesign: professional studio profile README for D4rk-Wolf"
```
