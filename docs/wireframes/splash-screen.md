# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Splash Screen

Version: 1.0

Status: Approved

---

# Purpose

The Splash Screen provides a calm, professional introduction to the application while assets and application data are loaded.

The splash screen should reinforce the Martin Dutton brand without overwhelming the user.

---

# Design Goals

The screen must feel:

* Calm
* Professional
* Reassuring
* Modern
* Minimalist

---

# Layout Structure

```text id="nkp74a"
┌─────────────────────┐
│                     │
│                     │
│                     │
│       ;             │
│                     │
│   Martin Dutton     │
│                     │
│ Clinical Psychologist│
│                     │
│                     │
│                     │
└─────────────────────┘
```

---

# Components

## Background

Colour:

```css id="4nt8rt"
#FCFCFA
```

Type:

Solid colour

---

## Logo

Component:

Semicolon Logo

Colour:

```css id="iw22c5"
#2E74B5
```

Position:

Centre

---

## Practice Name

Text:

```text id="3l44kq"
Martin Dutton
```

Typography:

Montserrat

Weight:

600

Size:

28px

Colour:

#333333

---

## Subtitle

Text:

```text id="q8jk7v"
Clinical Psychologist
```

Typography:

Montserrat

Weight:

500

Size:

18px

Colour:

#666666

---

# Loading Behaviour

Display Duration:

Minimum:

```text id="v9yxco"
1 second
```

Maximum:

```text id="5ibg7j"
3 seconds
```

---

## Exit Condition

Application ready

↓

Navigate to Home Screen

---

# Animation

## Allowed

Fade In

Duration:

300ms

---

## Not Allowed

* Bouncing
* Zoom effects
* Rotating elements
* Flashing elements

The splash screen should remain calm and subtle.

---

# Navigation

User Interaction:

None

No buttons

No links

No menus

---

# Accessibility

Requirements:

* High contrast text
* Readable typography
* Screen reader friendly

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Error Handling

If application fails to load:

Display:

```text id="pb7dvm"
Unable to load application.
Please try again.
```

Provide:

Retry Button

---

# Acceptance Criteria

The splash screen is complete when:

* Logo displays correctly
* Branding displays correctly
* Fade animation works
* Application transitions to Home Screen
* Layout scales correctly on mobile devices

---

# Navigation Map

Application Launch

↓

Splash Screen

↓

Home Screen

---

Status:

Approved for Development
