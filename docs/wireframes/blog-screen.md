# Martin Dutton Clinical Psychologist App

## Wireframe Specification

### Screen: Blog Screen

Version: 1.0

Status: Approved

---

# Purpose

The Blog Screen provides access to Martin's published articles and psychological insights.

Content is sourced automatically from:

```text
https://mjwdpsych.com/blog-feed.xml
```

The screen should encourage reading while remaining calm and uncluttered.

---

# Design Goals

The screen must feel:

* Informative
* Professional
* Calm
* Easy to browse

---

# Layout Structure

```text
┌─────────────────────┐
│                     │
│       Blog          │
│                     │
├─────────────────────┤
│ Search Articles     │
├─────────────────────┤
│ Featured Article    │
│                     │
│ Image               │
│ Title               │
│ Read Article →      │
├─────────────────────┤
│ Latest Articles     │
│                     │
│ Article Card        │
│ Article Card        │
│ Article Card        │
│ Article Card        │
├─────────────────────┤
│ Home Blog Book Contact │
└─────────────────────┘
```

---

# Components

## Screen Header

Title:

```text
Blog
```

Position:

Top Centre

Purpose:

Clearly identify the content section.

---

# Search Bar

## Component

SearchInput

Placeholder:

```text
Search articles...
```

Purpose:

Filter articles by title.

---

# Featured Article

## Component

FeaturedBlogCard

Data Source:

Most recent article from RSS feed.

### Fields

* Featured Image
* Title
* Excerpt
* Publication Date

### Action

Tap Card

↓

Open Article Reader

---

# Article List

## Component

BlogCard

Data Source:

RSS Feed

### Fields

* Featured Image
* Article Title
* Excerpt
* Publication Date

### Actions

Tap Card

↓

Open Article Reader

---

# RSS Feed Integration

Source:

```text
https://mjwdpsych.com/blog-feed.xml
```

Refresh Frequency:

Every 60 minutes

---

# Empty States

## No Articles Found

Display:

```text
No articles found.
```

---

## Search Returns No Results

Display:

```text
No matching articles found.
```

---

## RSS Feed Unavailable

Display:

```text
Articles are currently unavailable.
Please try again later.
```

---

# Loading States

## Featured Article

Skeleton Loader

---

## Article List

Skeleton Cards

Minimum:

3 placeholder cards

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

Blog

Colour:

```css
#2E74B5
```

---

## Inactive Items

Colour:

```css
#999999
```

---

# Accessibility

Requirements:

* Search field accessible
* All article cards keyboard accessible
* Screen reader support
* Alt text for images

---

# Responsive Behaviour

Supported:

* Android Phones
* iPhones
* Tablets

---

# Performance Requirements

Initial Load:

Less than 2 seconds

RSS Refresh:

Less than 5 seconds

---

# Acceptance Criteria

User can:

* Search articles
* Browse articles
* Open article reader
* Return to article list

RSS content displays correctly.

---

# Navigation Map

Blog Screen

├── Featured Article

│   └── Article Reader

│

└── Article List

```
└── Article Reader
```

---

Status:

Approved for Development
