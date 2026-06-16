# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen Group: Announcements

Version: 1.0

Status: Approved

---

# Purpose

The Announcement system allows Martin to communicate directly with patients through:

* Home Screen Highlights
* Announcement Archive
* Announcement Detail Screens
* Push Notifications

Announcements should be simple, clear and easy to read.

---

# Announcement Data Structure

## Fields

```text id="c7q2fa"
Title
Message
Category
Created Date
```

---

## Categories

Allowed Values:

```text id="f8m4pw"
general
appointment
blog
```

---

# Home Screen Announcement Card

## Purpose

Display the latest active announcement.

---

## Layout

```text id="q2w8nk"
┌─────────────────────┐
│ Latest Announcement │
│                     │
│ Title               │
│ Summary             │
│ Date                │
│                     │
│ View All →          │
└─────────────────────┘
```

---

## Actions

Tap Card

↓

Announcement Detail

---

Tap View All

↓

Announcement Archive

---

# Announcement Archive Screen

## Purpose

Display all active announcements.

---

# Layout Structure

```text id="s3n5vx"
┌─────────────────────┐
│                     │
│    Announcements    │
│                     │
├─────────────────────┤
│ Announcement Card   │
├─────────────────────┤
│ Announcement Card   │
├─────────────────────┤
│ Announcement Card   │
├─────────────────────┤
│ Announcement Card   │
└─────────────────────┘
```

---

# Components

## Header

Title:

```text id="m5p7qy"
Announcements
```

---

# Announcement Card

## Fields

* Title
* Summary
* Date

---

## Style

Background:

White

Radius:

```css id="t6v8jm"
16px
```

Shadow:

```css id="g4k9ce"
0 2px 8px rgba(0,0,0,0.05)
```

---

## Sorting

Newest First

---

## Actions

Tap Card

↓

Announcement Detail

---

# Announcement Detail Screen

## Purpose

Display the full announcement.

---

# Layout Structure

```text id="p8r2tn"
┌─────────────────────┐
│ ← Back              │
├─────────────────────┤
│ Title               │
│                     │
│ Date                │
│ Category            │
├─────────────────────┤
│                     │
│ Full Message        │
│                     │
├─────────────────────┤
│ Book Appointment    │
└─────────────────────┘
```

---

# Components

## Back Button

Action:

Return to previous screen.

---

## Announcement Header

### Fields

Title

Date

Category

---

### Typography

Title:

24px

Weight:

600

---

Date:

14px

Colour:

#666666

---

Category:

Badge Style

Background:

```css id="r4m7zh"
#EAF3FB
```

Text:

```css id="b9q5lf"
#2E74B5
```

---

# Announcement Content

## Source

Announcement Message

---

## Typography

Font:

Montserrat

Size:

16px

Line Height:

1.6

Colour:

#333333

---

# Book Appointment Button

## Component

PrimaryButton

Label:

```text id="n7v4qp"
Book Appointment
```

---

## Action

Open RecoMed

---

# Push Notification Flow

## Trigger

Announcement Published

---

## Notification

Title:

```text id="v3r8wy"
Martin Dutton Clinical Psychologist
```

---

Body:

```text id="h6p2ks"
New announcement available.
Tap to view.
```

---

## User Journey

Notification

↓

Tap Notification

↓

Announcement Detail Screen

---

# Empty States

## No Announcements

Display:

```text id="k5m8ra"
No announcements available.
```

---

# Announcement Not Found

Display:

```text id="s9x4tc"
Announcement unavailable.
```

Button:

```text id="w8q6pn"
Return Home
```

---

# Loading States

Archive:

Skeleton Cards

Count:

3

---

Detail:

Skeleton Header

Skeleton Content

---

# Accessibility

Requirements:

* Screen reader support
* Accessible buttons
* Accessible category badges
* Keyboard accessibility

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Acceptance Criteria

User can:

* View latest announcement
* Browse announcement archive
* Open announcement detail
* Open RecoMed from announcement
* Open announcement from push notification

---

# Navigation Map

Home Screen

├── Latest Announcement

│   └── Announcement Detail

│

└── View All

```
└── Announcement Archive

    └── Announcement Detail
```

---

Push Notification

↓

Announcement Detail

---

Status:

Approved for Development
