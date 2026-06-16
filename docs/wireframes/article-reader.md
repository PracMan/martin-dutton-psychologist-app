# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Article Reader

Version: 1.0

Status: Approved

---

# Purpose

The Article Reader screen displays the full content of a blog article sourced from the MJWD Psychology RSS feed.

The reading experience should feel:

* Calm
* Comfortable
* Professional
* Easy to read

The content itself should remain the primary focus.

---

# Design Goals

The screen must:

* Prioritize readability
* Minimize distractions
* Encourage article completion
* Support article sharing

---

# Layout Structure

```text id="q7z3lp"
┌─────────────────────┐
│ ← Back              │
├─────────────────────┤
│                     │
│ Hero Image          │
│                     │
├─────────────────────┤
│ Article Title       │
│                     │
│ Publication Date    │
├─────────────────────┤
│                     │
│ Article Content     │
│                     │
│                     │
│                     │
├─────────────────────┤
│ Share Article       │
└─────────────────────┘
```

---

# Components

## Back Button

Position:

Top Left

Label:

```text id="0wkh34"
Back
```

Action:

Return to Blog Screen

---

# Hero Image

## Component

ArticleHeroImage

Source:

RSS Feed

Purpose:

Visual introduction to article

---

# Article Header

## Fields

### Title

Source:

RSS Feed

Typography:

Montserrat

Weight:

600

Size:

24px

---

### Publication Date

Source:

RSS Feed

Typography:

Montserrat

Weight:

400

Size:

14px

Colour:

#666666

---

# Article Content

## Source

RSS Feed Content

---

## Formatting

Support:

* Paragraphs
* Headings
* Lists
* Links
* Images

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

# Share Button

## Component

PrimaryButton

Label:

```text id="fbvtn7"
Share Article
```

Action:

Open native device share dialog

---

# Content Behaviour

## Long Articles

Content scrolls vertically

---

## Images

Responsive

Scale to screen width

---

## External Links

Open in browser

---

# Navigation

## Entry Points

From:

* Featured Article
* Blog List

---

## Exit Points

Back

↓

Blog Screen

---

# Empty States

## Article Not Found

Display:

```text id="kx5wrj"
Article unavailable.
```

Button:

```text id="f3d87j"
Return to Blog
```

---

## RSS Error

Display:

```text id="lb2o8s"
Unable to load article.
Please try again later.
```

---

# Loading State

## Skeleton Layout

Display:

* Image Placeholder
* Title Placeholder
* Paragraph Placeholders

---

# Accessibility

Requirements:

* Screen reader support
* Accessible heading structure
* Accessible links
* Accessible images

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Performance Requirements

Article Load:

Less than 2 seconds

---

Image Load:

Lazy loading enabled

---

# Acceptance Criteria

User can:

* Read article
* Scroll content
* Share article
* Return to Blog Screen

RSS content displays correctly.

---

# Navigation Map

Blog Screen

↓

Article Reader

↓

Share Article

OR

↓

Back to Blog Screen

---

Status:

Approved for Development
