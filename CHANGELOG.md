# 📜 Changelog
All notable changes to **simplify.css** will be documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
and adheres to [Semantic Versioning](https://semver.org/).

---

## v1.1.0 | Nov 02, 2025
### 🔧 Improvements & Refinements

#### ✨ Overview
This update focuses on accessibility stability, framework compatibility, and cleanup of redundant resets — ensuring **simplify.css** remains safe to use across modern CSS libraries like Tailwind, MUI, Chakra, and Bootstrap.

#### 🧩 Changes
- **Typography**
  - Removed forced `line-height` from `body` to let frameworks manage text rhythm.
  - Retained `font-size: 1.6rem` for better scaling on modern layouts.
- **Forms & Interactive Elements**
  - Removed aggressive `user-select: none;` for accessibility (allows text selection again).
  - Switched `cursor: default` on disabled elements to `cursor: not-allowed`.
  - Simplified form control resets to preserve native behavior when needed.
- **Focus System**
  - Updated to rely on **system default outlines** for higher contrast compliance.
  - Retained `:focus-visible` for keyboard accessibility.
- **Media**
  - Split `svg` handling from other media for inline compatibility.
  - Added `vertical-align: middle;` to make SVG icons align naturally with text.
- **Lists & Tables**
  - Added `border-spacing: 0` for stricter table normalization.
  - Ensured lists have no left padding for cleaner framework alignment.
- **Removed Legacy Rules**
  - Dropped redundant line-height declarations and unnecessary vendor prefixes.
  - Removed over-opinionated resets that interfered with component libraries.

#### ✅ Summary
- **Safer defaults** — no override conflicts with utility frameworks.
- **More accessible** — keeps focus visibility and selection behaviors intact.
- **Cleaner spec alignment** — modernized resets with minimal overrides.

---

## v1.0.0 | Nov 02, 2025
### 🎉 Initial Stable Release

#### Overview
The first official release of **simplify.css** — a minimal, framework-agnostic baseline that corrects browser inconsistencies while keeping full design freedom.
Built for scalability, accessibility, and developer ergonomics.

#### ✨ Highlights
- **Predictable base scaling** — `1rem = 10px` for simpler math.
- **Universal `box-sizing: border-box`** — stable sizing for all elements.
- **Neutral baseline** — no fonts, colors, or spacing opinions.
- **Cross-framework compatibility** — works seamlessly with Tailwind, Bootstrap, MUI, Chakra, and more.
- **Accessible focus system** — visible outlines for keyboard users only.
- **Clean media defaults** — responsive `img`, `video`, `svg`, and `canvas` elements.
- **Safe isolation** for SPA mounts (`#root`, `#__next`) to prevent z-index bleed.
- **Unified form control reset** — removes inconsistent native appearances across browsers.
- **Consistent lists and tables** — neutral defaults for layout frameworks.
- **Utility safety rules** — hides `<template>` and `[hidden]` elements reliably.
