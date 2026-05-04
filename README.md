# MoleBio Toolkit

**Interactive Tools for Molecular Biology Lecture & Lab**

The MoleBio Toolkit is a focused, browser-based set of calculators and viewers for students studying molecular biology and biochemistry. Use it during lecture to step through translation in real time, or in the lab to set up a pipette, design a primer, plan a PCR, calculate a dilution, or mix a buffer — no login, no install, no signup.

**Live site:** [molebiolab.github.io/Toolkit](https://molebiolab.github.io/Toolkit)

---

## The Nine Tools

* **Central Dogma Flow** — animate DNA → RNA → protein. Includes a sickle-cell HBB demo with point-mutation classification (silent, missense, nonsense, frameshift).
* **Codon Table & Translator** — paste mRNA, step codon-by-codon or auto-translate, see the codon wheel update in real time. Hemoglobin β and GFP presets included.
* **Micropipette Viewer** — pixel-accurate P2 / P20 / P200 / P1000 dial visualization with range warnings, sliding tick marks, and Gilson-style digit windows showing the actual volume display.
* **Units & Molarity** — mass ↔ moles, molarity from mass, dilution (C₁V₁ = C₂V₂), mg/mL ↔ M conversions, and a Concentrate Mixer for loading dyes / sample buffers / restriction enzyme buffers (with optional top-up-to-volume mode). Pipettability checks flag below-P2 volumes and link to Serial Dilution. Common reagent presets included.
* **DNA Cloning & PCR** — primer melting temperature (forward + reverse) via SantaLucia 1998 nearest-neighbor thermodynamics with Owczarzy 2004 reciprocal-Tm salt correction. Detects self-complementary primers and applies the symmetry correction automatically. Pairs with a thermocycler planner: pick a polymerase (Taq / Phusion / Q5 / Platinum), enter amplicon length and cycle count, and get the full PCR program with extension time, time-per-cycle, and total run time.
* **Protein MW & pI** — molecular weight, isoelectric point, extinction coefficient (Pace et al. 1995, both reduced and oxidized), and a charge-vs-pH curve. Hemoglobin β and GFP presets included.
* **Serial Dilution** — visualize 4–10 tubes with log-scaled concentration shading, dilution-factor presets (1:2, 1:3, 1:5, 1:10, 1:100, custom), and a worked example showing the math. Cell-plating mode adds back-calculation from colony counts (CFU/mL via geometric mean of countable plates) and a transformation-efficiency calculator (CFU/µg DNA).
* **Buffer pH** — Henderson–Hasselbalch recipes for Tris-HCl, sodium phosphate, sodium acetate, HEPES, MES, bicarbonate, and custom buffers. Auto-detects whether the buffer is best made by **mixing** acid + conjugate base stocks or by **titrating** one form to pH with HCl/NaOH, and gives the right recipe for each. Includes a live titration curve with the pKa ± 1 buffering zone shaded.
* **Absorbance & Purity** — interactive UV spectrum (220–340 nm) for dsDNA / ssDNA / RNA / protein samples, with contamination presets (clean, +protein, +phenol, +salt). Real-time A₂₆₀/A₂₈₀ and A₂₆₀/A₂₃₀ ratio verdicts, plus Beer–Lambert concentration calculations using sample-specific extinction coefficients (50 / 33 / 40 µg·mL⁻¹·cm⁻¹) or user-supplied E¹% for proteins.

## Features

* **Single-file HTML** — no build step, no dependencies, no framework. Works offline once loaded.
* **Scientifically rigorous** — published nearest-neighbor parameters (SantaLucia 1998, Owczarzy 2004), Henderson–Hasselbalch with real biological pKa values, EMBOSS-style pKa values for pI, Pace et al. 1995 extinction coefficients, polymerase extension rates from manufacturer protocols.
* **Bench-realistic** — buffer recipes use 0.5/1/2/3 M stock dilutions (not powder weighings), pipette volumes flagged when below P2 minimums, PCR plans warn when amplicons exceed polymerase max range.
* **Installable** — PWA manifest + iOS web-app meta tags. Use "Add to Home Screen" on phones/tablets to launch as a standalone app.
* **Responsive** — works on desktop, laptop, tablet, and phone (down to 320 px).
* **Dark mode + high-contrast mode** — both saved across sessions.
* **Keyboard shortcuts** — `/` to search, `1`–`9` to jump between tools, `n`/`p` for next/previous, `h` for home, `?` for the settings menu, `Esc` to close modals.
* **Searchable** — type in the sidebar or click the mole mascot to find a tool by name or topic.
* **Accessible** — ARIA labels, skip-nav link, focus-visible outlines, `prefers-reduced-motion` honored, `prefers-contrast` supported.
* **Apple-friendly** — `viewport-fit=cover` for notched iPhones, `100dvh` for the iOS address bar, `-webkit-backdrop-filter` for older Safari, no auto-zoom on input focus.

## Tech Stack

Single-file vanilla HTML/CSS/JavaScript (~4,800 lines, ~280 KB; ~70 KB gzipped). No external dependencies at runtime. Google Fonts (DM Serif Display, DM Sans, DM Mono) load asynchronously with system fallbacks. Cookieless Google Analytics 4 tracks anonymous tool-open events to inform future improvements — no cookies, no cross-site tracking, no advertising.

## Usage

Visit the live site at [molebiolab.github.io/Toolkit](https://molebiolab.github.io/Toolkit), or clone and open locally:

```
git clone https://github.com/MoleBioLab/Toolkit.git
open index.html
```

The file works directly from disk (`file://`) in any modern browser, but features that depend on web context (link previews, Google Fonts, the PWA manifest) work best when served from a real URL.

## Companion Project

For the full 54-module biochemistry learning platform — pathway animators, 3D protein viewers, ball-and-stick molecular structures, and inline quizzes — see the main MoleBio site at [molebiolab.github.io/MoleBio](https://molebiolab.github.io/MoleBio).

The Toolkit and the platform are designed to complement each other: the platform teaches concepts, the Toolkit gets work done.

## Feedback

Found a scientific error? Have a feature suggestion?

* Open an [issue](https://github.com/MoleBioLab/Toolkit/issues) on this repo
* Or reach out via the About panel on the live site

## Author

**Dylan S. Blohm** — concept, curation, scientific direction, and design. Coded with Anthropic Claude.

© 2026 Dylan S. Blohm. All rights reserved.
