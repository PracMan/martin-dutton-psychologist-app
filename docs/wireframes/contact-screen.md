# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Contact Martin

Version: 1.0

Status: Approved

---

# Purpose

The Contact Screen provides patients with direct communication options.

The screen should make it easy for users to:

* Call Martin
* Send a WhatsApp message
* Send an Email

The design should remain simple and uncluttered.

---

# Design Goals

The screen must feel:

* Accessible
* Professional
* Friendly
* Easy to use

---

# Layout Structure

```text id="f6y2qv"
┌─────────────────────┐
│                     │
│  Contact Martin     │
│                     │
├─────────────────────┤
│                     │
│ 📞 Call             │
│                     │
├─────────────────────┤
│                     │
│ 💬 WhatsApp         │
│                     │
├─────────────────────┤
│                     │
│ ✉️ Email            │
│                     │
├─────────────────────┤
│ Home Blog Book Contact │
└─────────────────────┘
```

---

# Components

## Screen Header

Title:

```text id="9m7p2w"
Contact Martin
```

Position:

Top Centre

---

# Contact Card

## Component

ContactCard

Used for:

* Phone
* WhatsApp
* Email

Style:

* White Background
* Rounded Corners
* Light Shadow

Radius:

```css id="a2x5nv"
16px
```

---

# Phone Card

## Icon

Phone

---

## Label

```text id="q1f9kr"
Call Martin
```

---

## Action

Tap

↓

Open Device Dialer

---

## URI

```text id="p3l0sz"
tel:{PHONE_NUMBER}
```

---

# WhatsApp Card

## Icon

WhatsApp

---

## Label

```text id="u4c8bx"
WhatsApp Martin
```

---

## Action

Tap

↓

Open WhatsApp

---

## URI

```text id="q7r5mk"
https://wa.me/{WHATSAPP_NUMBER}
```

---

# Email Card

## Icon

Email

---

## Label

```text id="z2n8tp"
Email Martin
```

---

## Action

Tap

↓

Open Email Application

---

## URI

```text id="g9w4cu"
mailto:{EMAIL_ADDRESS}
```

---

# Contact Data

Values stored in:

Environment Configuration

or

Application Settings

---

Fields:

```text id="r8t3yk"
PHONE_NUMBER

WHATSAPP_NUMBER

EMAIL_ADDRESS
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

## Active Item

Contact

Colour:

```css id="m5p9hj"
#2E74B5
```

---

## Inactive Items

Colour:

```css id="v7k2nr"
#999999
```

---

# Error States

## Phone Unavailable

Display:

```text id="c4q7zd"
Phone number unavailable.
```

---

## WhatsApp Unavailable

Display:

```text id="e8w6ts"
WhatsApp unavailable.
```

---

## Email Unavailable

Display:

```text id="j1x3lu"
Email unavailable.
```

---

# Loading State

Display:

Skeleton Cards

Count:

3

---

# Accessibility

Requirements:

* Screen reader labels
* Minimum touch targets of 44px
* High contrast text
* Keyboard accessibility

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Performance Requirements

Screen Load:

Less than 1 second

---

# Acceptance Criteria

User can:

* Call Martin
* Open WhatsApp
* Send Email

All contact actions launch the correct application.

---

# Navigation Map

Home

↓

Contact Screen

├── Phone Dialer

├── WhatsApp

└── Email Application

---

Status:

Approved for Development
