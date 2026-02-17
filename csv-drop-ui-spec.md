# 📦 CSV Drop Interface -- Front-End Specification

**Project:** CSV Upload Portal\
**Version:** 1.0\
**Scope:** Front-end only (no backend integration yet)\
**Goal:** Professional, standalone, production-quality UI

------------------------------------------------------------------------

# 1. 🎯 Project Objective

Create a modern, clean, professional CSV file upload interface.

This is a **standalone front-end application**.\
Backend/API integration will be added later.

The UI must: - Look enterprise-grade - Be minimal but visually strong -
Clearly communicate upload state - Be responsive - Include visual
feedback animations

------------------------------------------------------------------------

# 2. 🧱 Layout Structure

## Page Layout

    ------------------------------------------------
    | Header                                       |
    |----------------------------------------------|
    |                                              |
    |          Main Upload Card (Centered)        |
    |                                              |
    |----------------------------------------------|
    | Footer                                       |
    ------------------------------------------------

------------------------------------------------------------------------

# 3. 🎨 Design System

## Typography

  Element      Font              Weight   Size
  ------------ ----------------- -------- ------
  Heading      Inter / Poppins   600      28px
  Subheading   Inter             400      16px
  Body         Inter             400      14px
  Button       Inter             500      14px

Fallback:

    font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;

------------------------------------------------------------------------

## Colour Palette

  Purpose          Colour
  ---------------- ---------
  Primary          #1E3A8A
  Accent           #2563EB
  Success          #16A34A
  Error            #DC2626
  Background       #F8FAFC
  Card             #FFFFFF
  Border           #E2E8F0
  Text Primary     #0F172A
  Text Secondary   #64748B

------------------------------------------------------------------------

# 4. 🖼 Main Upload Card Design

## Card Specs

-   Width: 480px
-   Padding: 40px
-   Border radius: 16px
-   Shadow:

```{=html}
<!-- -->
```
    box-shadow: 0 10px 25px rgba(0,0,0,0.08);

-   Background: White

------------------------------------------------------------------------

## Inside Card Layout

    [ Upload Icon ]

    Upload Your CSV File

    Drag & drop your file here
    or

    [ Browse Files Button ]

    Supported format: .csv
    Max file size: 10MB

------------------------------------------------------------------------

# 5. 🧲 Drag & Drop Behaviour

### Default State

-   Dashed border
-   Subtle grey background
-   Upload icon visible

### Hover / Drag Over State

-   Border turns Accent Blue
-   Background light blue tint
-   Slight scale animation (1.02)

### Success State

-   Border turns green
-   Success check icon appears
-   File name displayed
-   "Ready to process" label shown

### Error State

-   Border red
-   Error message below box

------------------------------------------------------------------------

# 6. 🧠 Functional Behaviour (Front-End Only)

### Validation Rules

-   Accept only `.csv`
-   Max size: 10MB
-   Show error message if invalid

### On Successful Upload

-   Display:

    -   File name
    -   File size

-   Show:

        File ready for processing

### Placeholder Backend Hook

``` javascript
function handleCSVUpload(file) {
  console.log("CSV file ready:", file);
  // TODO: Connect to backend API endpoint
}
```

------------------------------------------------------------------------

# 7. 💡 Visual Enhancements

-   Smooth hover transitions (200ms ease)
-   Subtle micro-animations
-   Clean SVG upload icon
-   Light gradient background:

```{=html}
<!-- -->
```
    background: linear-gradient(135deg, #F8FAFC 0%, #EEF2FF 100%);

------------------------------------------------------------------------

# 8. 📱 Responsive Design

### Desktop

Centered card.

### Tablet

Card width: 90%.

### Mobile

-   Full width
-   Reduced padding (24px)

------------------------------------------------------------------------

# 9. 📁 File Structure

    /csv-drop-ui
    │
    ├── index.html
    ├── styles.css
    ├── script.js
    └── README.md

------------------------------------------------------------------------

# 10. 🚀 README.md

# CSV Drop Interface

## Overview

This is a standalone front-end CSV upload interface.

It is designed to: - Accept CSV files - Validate file type and size -
Provide visual feedback - Prepare for backend integration

------------------------------------------------------------------------

## Setup

1.  Clone or download project.
2.  Open `index.html` in browser.
3.  No dependencies required.

------------------------------------------------------------------------

## How It Works

-   Drag & drop a CSV file into the upload box.
-   Or click "Browse Files".
-   File is validated on the client side.
-   UI updates to reflect upload state.

------------------------------------------------------------------------

## Current Limitations

-   No backend processing yet.
-   No database connection.
-   No server upload.

------------------------------------------------------------------------

## Next Phase (Backend Integration)

Planned:

-   POST file to `/api/upload`
-   Display processing spinner
-   Parse CSV
-   Return validation report
-   Show row count preview

------------------------------------------------------------------------

## Customisation

You can modify:

-   Colours in `styles.css`
-   File size limit in `script.js`
-   API endpoint in `handleCSVUpload()`

------------------------------------------------------------------------

# 11. 🔒 Future Upgrade Path

-   CSV preview table (first 10 rows)
-   Schema validation
-   Upload progress bar
-   Authentication gate
-   Drag multiple files
-   Dark mode toggle
