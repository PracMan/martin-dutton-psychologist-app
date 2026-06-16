# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: New Announcement

Version: 1.0

Status: Approved

---

# Purpose

The New Announcement screen allows Martin to create and publish announcements that will:

* Appear on the Home Screen
* Appear in the Announcement Archive
* Generate a Push Notification
* Be available immediately to users

The workflow should be fast and require minimal administrative effort.

---

# Design Goals

The screen must feel:

* Efficient
* Professional
* Simple
* Reliable

Publishing an announcement should take less than one minute.

---

# Layout Structure

```text id="m6p4xk"
┌─────────────────────┐
│                     │
│  New Announcement   │
│                     │
├─────────────────────┤
│ Title               │
├─────────────────────┤
│ Category            │
├─────────────────────┤
│ Message             │
│                     │
│                     │
│                     │
├─────────────────────┤
│ Publish Announcement│
└─────────────────────┘
```

---

# Components

## Screen Header

Title:

```text id="f7q3nt"
New Announcement
```

Position:

Top Centre

---

# Title Field

## Component

TextInput

Label:

```text id="t2w9ck"
Title
```

---

## Validation

Required

Minimum:

```text id="a8n4vx"
3 characters
```

Maximum:

```text id="d5p7zr"
120 characters
```

---

## Example

```text id="j9m2qw"
Additional Evening Appointments Available
```

---

# Category Field

## Component

DropdownSelect

Label:

```text id="u4x8mk"
Category
```

---

## Allowed Values

```text id="v3r6pq"
General
Appointment
Blog
```

---

## Default Value

```text id="b9t5nv"
General
```

---

# Message Field

## Component

TextArea

Label:

```text id="n6p8wy"
Message
```

---

## Validation

Required

Minimum:

```text id="q1m7vk"
10 characters
```

Maximum:

```text id="g5w9xp"
5000 characters
```

---

## Example

```text id="c2v4rn"
Additional evening appointments are now available for booking through RecoMed.
```

---

# Publish Button

## Component

PrimaryButton

Label:

```text id="z8p6tk"
Publish Announcement
```

---

## Action

Tap

↓

Validate Form

↓

Save Announcement

↓

Send Notification

↓

Return to Dashboard

---

# Publishing Workflow

## Step 1

Validate Input

---

Required:

* Title
* Category
* Message

---

## Step 2

Insert Record

Table:

```text id="m4x9wc"
announcements
```

---

## Step 3

Generate Push Notification

Provider:

Firebase Cloud Messaging

---

## Step 4

Update Home Screen

Latest Announcement

---

## Step 5

Update Announcement Archive

Display new announcement

---

## Step 6

Return to Dashboard

---

# Notification Generated

## Title

```text id="y5k2nv"
Martin Dutton Clinical Psychologist
```

---

## Body

```text id="w8r4pt"
New announcement available.
Tap to view.
```

---

## Deep Link

```text id="p7m3xq"
/announcements/{announcementId}
```

---

# Success State

Display:

```text id="r4t8vk"
Announcement published successfully.
```

---

Redirect:

```text id="j6w9pn"
/admin/dashboard
```

---

# Validation Errors

## Missing Title

Display:

```text id="v2p7qm"
Please enter a title.
```

---

## Missing Message

Display:

```text id="m8r4tx"
Please enter a message.
```

---

## Invalid Category

Display:

```text id="q5w8nk"
Please select a category.
```

---

# System Errors

## Database Error

Display:

```text id="c9v3pk"
Unable to publish announcement.
Please try again.
```

---

## Notification Failure

Display:

```text id="u7m5wr"
Announcement published.
Notification delivery failed.
```

Announcement remains published.

---

# Loading State

## Publish Button

Display:

```text id="x3p8qt"
Publishing...
```

Button disabled.

---

# Security Requirements

Authentication Required

---

Protected Route:

```text id="k4v9nm"
/admin/announcements/new
```

---

Unauthenticated Users:

Redirect

↓

```text id="b7w2pk"
/admin
```

---

# Accessibility

Requirements:

* Accessible form labels
* Keyboard navigation
* Visible focus states
* Screen reader support

---

# Responsive Behaviour

Supported:

* Desktop
* Laptop
* Tablet
* Mobile

Primary target:

Desktop

---

# Performance Requirements

Publish Time:

Less than 2 seconds

---

Notification Trigger:

Less than 30 seconds

---

# Acceptance Criteria

Administrator can:

* Enter title
* Select category
* Enter message
* Publish announcement
* Trigger push notification
* Return to dashboard

---

# Navigation Map

Dashboard

↓

New Announcement

↓

Publish

├── Save Announcement

├── Send Notification

├── Update Home Screen

├── Update Archive

└── Return Dashboard

---

Status:

Approved for Development
