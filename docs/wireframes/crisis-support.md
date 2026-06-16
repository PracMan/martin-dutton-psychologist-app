# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Crisis Support

Version: 1.0

Status: Approved

---

# Purpose

The Crisis Support screen provides immediate access to emergency and mental health support services.

This screen should prioritize:

* Speed
* Clarity
* Accessibility
* Simplicity

The user should be able to contact a support service in one tap.

---

# Design Goals

The screen must feel:

* Calm
* Reassuring
* Professional
* Easy to navigate

The screen must avoid:

* Excessive information
* Long paragraphs
* Complex navigation

---

# Layout Structure

```text id="g8p3yz"
┌─────────────────────┐
│                     │
│   Crisis Support    │
│                     │
├─────────────────────┤
│ If this is an       │
│ emergency call      │
│ emergency services  │
├─────────────────────┤
│ Emergency Services  │
├─────────────────────┤
│ SADAG               │
├─────────────────────┤
│ Lifeline SA         │
├─────────────────────┤
│ Childline SA        │
├─────────────────────┤
│ Home Blog Book Contact │
└─────────────────────┘
```

---

# Components

## Screen Header

Title:

```text id="m2f7rk"
Crisis Support
```

Position:

Top Centre

---

# Emergency Banner

## Component

EmergencyBanner

Purpose:

Provide immediate guidance.

---

## Message

```text id="v5h9ct"
If you are in immediate danger or experiencing a medical emergency, please contact emergency services immediately.
```

---

## Style

Background:

Light Blue

Border:

Primary Brand Colour

---

# Crisis Contact Cards

## Component

CrisisSupportCard

Style:

* White Background
* Rounded Corners
* Light Shadow

Radius:

```css id="a8w6zn"
16px
```

---

# Emergency Services

## Label

```text id="d3x1jp"
Emergency Services
```

---

## Action

Tap

↓

Open Phone Dialer

---

## URI

```text id="v9m7ly"
tel:{EMERGENCY_NUMBER}
```

---

# SADAG

## Label

```text id="w4r8nt"
SADAG
```

---

## Description

South African Depression and Anxiety Group

---

## Action

Tap

↓

Open Phone Dialer

---

# Lifeline South Africa

## Label

```text id="x7c3pv"
Lifeline South Africa
```

---

## Action

Tap

↓

Open Phone Dialer

---

# Childline South Africa

## Label

```text id="q6n5kd"
Childline South Africa
```

---

## Action

Tap

↓

Open Phone Dialer

---

# Contact Data

Values stored in:

Application Configuration

---

Fields

```text id="k2w8fz"
EMERGENCY_NUMBER

SADAG_NUMBER

LIFELINE_NUMBER

CHILDLINE_NUMBER
```

---

# Navigation

## Bottom Navigation

Items:

* Home
* Blog
* Book
* Contact

---

## Active Navigation

None

This screen is accessed through:

* Home Screen Quick Action
* Contact Screen Links
* Deep Links (Future)

---

# Empty States

## Contact Number Missing

Display:

```text id="n8q2mv"
Support number currently unavailable.
```

---

# Loading State

Display:

Skeleton Contact Cards

Count:

4

---

# Accessibility

Requirements:

* High contrast text
* Screen reader labels
* Large touch targets
* Keyboard accessibility

Minimum Touch Target:

```css id="r5t9jx"
44px
```

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Performance Requirements

Load Time:

Less than 1 second

---

# Acceptance Criteria

User can:

* View emergency guidance
* Call Emergency Services
* Call SADAG
* Call Lifeline South Africa
* Call Childline South Africa

All contact options launch the phone dialer correctly.

---

# Navigation Map

Home Screen

↓

Crisis Support

├── Emergency Services

├── SADAG

├── Lifeline South Africa

└── Childline South Africa

↓

Phone Dialer

---

Status:

Approved for Development
