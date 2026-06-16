# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Admin Login

Version: 1.0

Status: Approved

---

# Purpose

The Admin Login screen provides secure access to the administration portal.

Only authorised users may access:

* Dashboard
* Announcement Management
* Publishing Functions

Version 1 supports a single administrator account.

---

# Design Goals

The screen must feel:

* Professional
* Secure
* Minimalist
* Consistent with the public application

---

# Layout Structure

```text id="p4k7wx"
┌─────────────────────┐
│                     │
│         ;           │
│                     │
│  Martin Dutton      │
│                     │
│ Clinical Psychologist│
│                     │
├─────────────────────┤
│ Email Address       │
├─────────────────────┤
│ Password            │
├─────────────────────┤
│                     │
│      Log In         │
│                     │
├─────────────────────┤
│ Forgot Password?    │
└─────────────────────┘
```

---

# Components

## Logo

Component:

Semicolon Logo

Colour:

```css id="n7x2zp"
#2E74B5
```

Position:

Top Centre

---

# Practice Name

Text:

```text id="j4w8nm"
Martin Dutton
```

Typography:

Montserrat

Weight:

600

Size:

24px

---

# Subtitle

Text:

```text id="s5v9qh"
Clinical Psychologist
```

Typography:

Montserrat

Weight:

500

Size:

16px

Colour:

#666666

---

# Email Field

## Component

TextInput

Label:

```text id="m8r4yc"
Email Address
```

Type:

Email

Validation:

Required

---

# Password Field

## Component

PasswordInput

Label:

```text id="t2q6vk"
Password
```

Type:

Password

Validation:

Required

---

# Login Button

## Component

PrimaryButton

Label:

```text id="v7m1pe"
Log In
```

Action:

Authenticate via Supabase Auth

---

# Forgot Password Link

## Component

Text Link

Label:

```text id="q8n3bt"
Forgot Password?
```

Action:

Open password reset flow

---

# Authentication Flow

User enters:

* Email
* Password

↓

Tap Log In

↓

Supabase Authentication

---

## Success

Redirect:

```text id="w6k2yr"
/admin/dashboard
```

---

## Failure

Display Error:

```text id="h3p8zx"
Invalid email or password.
```

---

# Loading State

## Login Button

Display:

```text id="r9w5cv"
Signing In...
```

Button disabled during authentication.

---

# Error States

## Invalid Credentials

Display:

```text id="k4x7nm"
Invalid email or password.
```

---

## Network Error

Display:

```text id="u5v2rz"
Unable to sign in.
Please try again.
```

---

## Session Expired

Display:

```text id="y8m6qt"
Your session has expired.
Please sign in again.
```

---

# Security Requirements

Authentication Provider:

Supabase Auth

---

Session Management:

Secure HTTP-only cookies

---

Protected Routes:

```text id="z7p4wj"
/admin/dashboard
/admin/announcements/new
```

---

# Accessibility

Requirements:

* Screen reader support
* Accessible form labels
* Keyboard navigation
* Visible focus states

---

# Responsive Behaviour

Supported:

* Desktop
* Laptop
* Tablet
* Mobile

---

# Acceptance Criteria

Administrator can:

* Enter email
* Enter password
* Authenticate successfully
* Access dashboard
* Reset password

Unauthenticated users cannot access protected routes.

---

# Navigation Map

Admin Login

↓

Authenticate

├── Success

│   └── Dashboard

│

└── Failure

```
└── Error Message
```

---

Status:

Approved for Development
