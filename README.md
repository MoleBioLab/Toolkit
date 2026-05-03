# MoleBio Toolkit

**Interactive Tools for Molecular Biology Lecture & Lab**

The MoleBio Toolkit is a focused, browser-based set of calculators and viewers for students studying molecular biology and biochemistry. Use it during lecture to step through translation in real time, or in the lab to set up a pipette, design a primer, or calculate a dilution — no login, no install, no signup.

**Live site:** [molebiolab.github.io/Toolkit](https://molebiolab.github.io/Toolkit)

---

## The Six Tools

* **Central Dogma Flow** — animate DNA → RNA → protein. Includes a sickle-cell HBB demo with point-mutation classification (silent, missense, nonsense, frameshift).
* **Codon Table & Translator** — paste mRNA, step codon-by-codon or auto-translate, see the codon wheel update in real time. Hemoglobin β and GFP presets included.
* **Micropipette Viewer** — pixel-accurate P2 / P20 / P200 / P1000 dial visualization with range warnings and tick math.
* **Units & Molarity** — mass ↔ moles, molarity from mass, dilution (C₁V₁ = C₂V₂), and mg/mL ↔ M conversions. Common reagent presets (NaCl, Tris, glucose, HEPES, BSA).
* **DNA Tm Calculator** — primer melting temperature via SantaLucia 1998 nearest-neighbor thermodynamics with Owczarzy 2004 reciprocal-Tm salt correction. Detects self-complementary primers and applies the symmetry correction automatically.
* **Protein MW & pI** — molecular weight, isoelectric point, extinction coefficient (Pace et al. 1995, both reduced and oxidized), and a charge-vs-pH curve. Hemoglobin β and GFP presets included.

## Features

* **Single-file HTML** — no build step, no dependencies, no framework. Works offline once loaded.
* **Scientifically rigorous** — published nearest-neighbor parameters, EMBOSS-style pKa values for pI, real preset sequences with verified translations.
* **Responsive** — works on desktop, laptop, tablet, and phone (down to 320 px).
* **Dark mode + high-contrast mode** — both saved across sessions.
* **Keyboard shortcuts** — `/` to search, `1`–`6` to jump between tools, `?` for the settings menu, `Esc` to close modals.
* **Searchable** — type in the sidebar or click the mole mascot to find a tool by name or topic.
* **Accessible** — ARIA labels, skip-nav link, focus-visible outlines, `prefers-reduced-motion` honored, `prefers-contrast` supported.
* **Apple-friendly** — `viewport-fit=cover` for notched iPhones, `100dvh` for the iOS address bar, `-webkit-backdrop-filter` for older Safari, no auto-zoom on input focus.

## Tech Stack

Single-file vanilla HTML/CSS/JavaScript (~3,000 lines, ~165 KB). No external dependencies at runtime. Google Fonts (DM Serif Display, DM Sans, DM Mono) load asynchronously with system fallbacks.

## Usage

Visit the live site at [molebiolab.github.io/Toolkit](https://molebiolab.github.io/Toolkit), or clone and open locally:

```
git clone https://github.com/MoleBioLab/Toolkit.git
open index.html
```

The file works directly from disk (`file://`) in any modern browser, but features that depend on web context (link previews, Google Fonts, future deep-linking) work best when served from a real URL.

## Companion Project

For the full 54-module biochemistry learning platform — pathway animators, 3D protein viewers, ball-and-stick molecular structures, and inline quizzes — see the main MoleBio site at [molebiolab.github.io/MoleBio](https://molebiolab.github.io/MoleBio).

The Toolkit and the platform are designed to complement each other: the platform teaches concepts, the Toolkit gets work done.

## Feedback

Found a scientific error? Have a feature suggestion?

* Open an [issue](https://github.com/MoleBioLab/Toolkit/issues) on this repo
* Or reach out via the About panel on the live site

## Author

**Dylan S. Blohm** — concept, scientific direction, and design. Coded with Anthropic Claude.

© 2026 Dylan S. Blohm. All rights reserved.
