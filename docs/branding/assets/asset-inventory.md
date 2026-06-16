# Martin Dutton Clinical Psychologist App

## Asset Inventory v1.0

### Document Information

| Item     | Value           |
| -------- | --------------- |
| Document | Asset Inventory |
| Version  | 1.0             |
| Status   | Approved        |

---

# 1. Purpose

This document provides a complete inventory of all visual assets required for Version 1.0 of the Martin Dutton Clinical Psychologist App.

It serves as the master reference for:

* Designers
* Developers
* QA Testing
* Deployment Validation

---

# 2. Asset Categories

The application requires the following asset groups:

1. Logo Assets
2. Application Icons
3. Splash Assets
4. Browser Assets
5. UI Assets
6. Documentation Assets

---

# 3. Logo Assets

Location:

```text
public/logos/
```

| Asset                    | Format | Required |
| ------------------------ | ------ | -------- |
| semicolon.svg            | SVG    | Yes      |
| semicolon.png            | PNG    | Yes      |
| heartbeat-logo.svg       | SVG    | Yes      |
| heartbeat-logo.png       | PNG    | Yes      |
| full-logo-horizontal.svg | SVG    | Yes      |
| full-logo-horizontal.png | PNG    | Yes      |

---

## Semicolon Logo

Purpose:

* App branding
* App icon source
* Splash screen
* Login screen
* Home screen

Status:

Required

---

## Heartbeat Logo

Purpose:

* Practice branding
* Marketing material
* Documentation

Status:

Required

---

## Full Horizontal Logo

Purpose:

* Website header
* Documentation
* Presentations

Status:

Required

---

# 4. Application Icons

Location:

```text
public/icons/
```

| Asset                | Size      | Format | Required |
| -------------------- | --------- | ------ | -------- |
| app-icon-1024.png    | 1024×1024 | PNG    | Yes      |
| icon-512.png         | 512×512   | PNG    | Yes      |
| icon-192.png         | 192×192   | PNG    | Yes      |
| apple-touch-icon.png | 180×180   | PNG    | Yes      |
| maskable-icon.png    | 512×512   | PNG    | Yes      |

---

## Source Asset

Master source:

```text
app-icon-1024.png
```

All icon exports originate from this file.

---

# 5. Browser Assets

Location:

```text
public/icons/
```

| Asset          | Size       | Required |
| -------------- | ---------- | -------- |
| favicon.ico    | Multi-size | Yes      |
| favicon-32.png | 32×32      | Yes      |

---

# 6. Splash Assets

Location:

```text
public/splash/
```

| Asset                       | Format | Required |
| --------------------------- | ------ | -------- |
| splash-logo.svg             | SVG    | Yes      |
| splash-screen-reference.png | PNG    | Yes      |

---

## Splash Logo

Purpose:

Application startup branding.

---

## Splash Reference

Purpose:

Developer reference.

Used to verify implementation matches approved design.

---

# 7. UI Assets

Location:

```text
public/images/
```

| Asset                        | Format | Required |
| ---------------------------- | ------ | -------- |
| emergency-banner.svg         | SVG    | Yes      |
| blog-placeholder.jpg         | JPG    | Optional |
| announcement-placeholder.jpg | JPG    | Optional |

---

## Emergency Banner

Purpose:

Crisis Support screen.

Status:

Required

---

# 8. Documentation Assets

Location:

```text
docs/branding/assets/
```

| Asset                  | Purpose             |
| ---------------------- | ------------------- |
| branding-guidelines.md | Brand standards     |
| colour-palette.md      | Colour definitions  |
| logo-usage.md          | Logo usage rules    |
| asset-inventory.md     | Asset inventory     |
| icon-specifications.md | Icon specifications |
| logo-specifications.md | Logo specifications |
| export-checklist.md    | Export validation   |

---

# 9. Repository Structure

```text
public/
│
├── icons/
│   ├── app-icon-1024.png
│   ├── icon-512.png
│   ├── icon-192.png
│   ├── apple-touch-icon.png
│   ├── maskable-icon.png
│   ├── favicon.ico
│   └── favicon-32.png
│
├── logos/
│   ├── semicolon.svg
│   ├── semicolon.png
│   ├── heartbeat-logo.svg
│   ├── heartbeat-logo.png
│   ├── full-logo-horizontal.svg
│   └── full-logo-horizontal.png
│
├── splash/
│   ├── splash-logo.svg
│   └── splash-screen-reference.png
│
└── images/
    ├── emergency-banner.svg
    ├── blog-placeholder.jpg
    └── announcement-placeholder.jpg
```

---

# 10. Asset Production Status

## Logos

* [ ] semicolon.svg
* [ ] semicolon.png
* [ ] heartbeat-logo.svg
* [ ] heartbeat-logo.png
* [ ] full-logo-horizontal.svg
* [ ] full-logo-horizontal.png

---

## Icons

* [ ] app-icon-1024.png
* [ ] icon-512.png
* [ ] icon-192.png
* [ ] apple-touch-icon.png
* [ ] maskable-icon.png

---

## Browser

* [ ] favicon.ico
* [ ] favicon-32.png

---

## Splash

* [ ] splash-logo.svg
* [ ] splash-screen-reference.png

---

## UI

* [ ] emergency-banner.svg

---

# 11. Acceptance Criteria

Asset package is complete when:

* All required assets exist
* Assets are stored in correct folders
* Assets meet specification documents
* Assets pass export checklist
* Assets are committed to GitHub

---

# Version History

## Version 1.0

Initial approved asset inventory.

Status:

Ready for Asset Production
