# Martin Dutton Clinical Psychologist App

## Colour Palette v1.0

### Document Information

| Item     | Value          |
| -------- | -------------- |
| Document | Colour Palette |
| Version  | 1.0            |
| Status   | Approved       |

---

# 1. Overview

This document defines all approved colours for the Martin Dutton Clinical Psychologist App.

The colour palette is intentionally restrained to promote:

* Calmness
* Professionalism
* Readability
* Accessibility

Only colours defined in this document may be used in production.

---

# 2. Primary Brand Colour

## Martin Blue

Purpose:

Primary brand colour.

Used for:

* Logo
* Buttons
* Links
* Icons
* Active Navigation
* Highlights

---

### HEX

```css id="j6w2pn"
#2E74B5
```

---

### RGB

```css id="q4r9mk"
46, 116, 181
```

---

### Tailwind

```js id="z8v3tn"
primary: '#2E74B5'
```

---

# 3. Background Colours

## Primary Background

Purpose:

Application background

---

### HEX

```css id="u3k7vq"
#FCFCFA
```

---

## Card Background

Purpose:

Cards and containers

---

### HEX

```css id="m5n8rx"
#FFFFFF
```

---

# 4. Text Colours

## Primary Text

Used for:

* Headings
* Body text

---

### HEX

```css id="c7v2wp"
#333333
```

---

## Secondary Text

Used for:

* Dates
* Labels
* Supporting text

---

### HEX

```css id="f4q9nm"
#666666
```

---

## Disabled Text

Used for:

* Disabled controls

---

### HEX

```css id="w2k8rv"
#999999
```

---

# 5. Border Colours

## Standard Border

Used for:

* Cards
* Inputs
* Dividers

---

### HEX

```css id="n9p3wx"
#E6E6E6
```

---

# 6. Status Colours

## Success

Used for:

* Successful actions
* Confirmation messages

---

### HEX

```css id="t5m7pk"
#2F855A
```

---

## Warning

Used for:

* Non-critical alerts

---

### HEX

```css id="r8v4qn"
#DD6B20
```

---

## Error

Used for:

* Validation errors
* System failures

---

### HEX

```css id="k6x2mr"
#C53030
```

---

# 7. Category Badge Colours

## General

Background:

```css id="v9n5qx"
#EAF3FB
```

Text:

```css id="b7m4rk"
#2E74B5
```

---

## Appointment

Background:

```css id="p2v8wn"
#EEF7EE
```

Text:

```css id="d5k9qt"
#2F855A
```

---

## Blog

Background:

```css id="h4x7mp"
#FFF4E6
```

Text:

```css id="s3n8rv"
#DD6B20
```

---

# 8. Navigation Colours

## Active Navigation

### HEX

```css id="q8w2pk"
#2E74B5
```

---

## Inactive Navigation

### HEX

```css id="m7v4xn"
#999999
```

---

# 9. Button Colours

## Primary Button

Background:

```css id="c4p9wm"
#2E74B5
```

Text:

```css id="x6k2rn"
#FFFFFF
```

---

## Secondary Button

Background:

```css id="n3v8qp"
#FFFFFF
```

Border:

```css id="u9m4xt"
#2E74B5
```

Text:

```css id="f5w7pk"
#2E74B5
```

---

# 10. Accessibility

All colour combinations must meet:

WCAG AA

Minimum contrast ratio:

```text id="p8v3mq"
4.5:1
```

---

# 11. Tailwind Configuration

```javascript id="g2k7rx"
colors: {
  primary: '#2E74B5',
  background: '#FCFCFA',
  surface: '#FFFFFF',
  text: '#333333',
  secondaryText: '#666666',
  border: '#E6E6E6',
  success: '#2F855A',
  warning: '#DD6B20',
  error: '#C53030'
}
```

---

# 12. Approved Usage

Developers must:

* Use colours from this document only
* Maintain consistency across screens
* Follow accessibility requirements

---

# Version History

## Version 1.0

Initial approved colour palette.

Status:

Ready for Development
