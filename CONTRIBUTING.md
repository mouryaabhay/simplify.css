# 🤝 Contributing to simplify.css

Thank you for your interest in contributing to **simplify.css**!
This project exists to provide a stable, framework-agnostic CSS foundation that improves consistency without enforcing design opinions.

This document outlines how to contribute effectively and responsibly, ensuring Simplify.css remains lightweight, consistent, and scalable.

---

## 🧭 Guiding Principles

Simplify.css is built around a few non-negotiable values:

| Principle | Description |
|------------|-------------|
| 🧱 **Consistency Over Style** | We fix inconsistencies — not redesign defaults. Simplify.css ensures a stable foundation without dictating appearance. |
| ⚙️ **Predictability First** | Every declaration should have a clear, measurable purpose — no arbitrary “looks better” changes. |
| 🧩 **Framework Neutrality** | It must integrate seamlessly with any ecosystem: Tailwind, MUI, Bootstrap, React, Vue, etc. |
| ♿ **Accessibility Matters** | Preserve accessibility defaults, focus outlines, and readable scaling. Never hide user cues. |
| 📏 **1rem = 10px Logic** | The base scaling system should simplify math and spacing — not introduce visual bias. |
| 💬 **Clarity in Code** | Comment only when intent isn’t self-evident; prioritize clean, readable CSS. |

If a proposed change breaks, overrides, or duplicates a framework’s default — it probably doesn’t belong in Simplify.css.

---

## 🪲 Reporting Issues

Found a bug, inconsistency, or unexpected browser behavior? Great — that helps everyone.

Please use the GitHub **Issues** tab, and before opening a new one:

1. **Search existing issues** to avoid duplicates.
2. **Check the latest `main` branch** — your issue may already be fixed.
3. **Isolate the problem** with a minimal reproduction.

**Good issue reports include:**
- A clear, descriptive title
- Steps to reproduce the issue
- Expected vs. actual behavior
- A live demo (CodePen, JSFiddle, etc.)
- Browser(s), OS, and rendering context (e.g. mobile/desktop)

**Example:**
> **Title:** Button alignment inconsistent in Safari 17.3
>
> **Steps to Reproduce:**
> 1. Import `simplify.css`
> 2. Add a native `<button>` element
> 3. Compare layout across Safari and Chrome
>
> **Expected:** Equal padding and vertical alignment
> **Actual:** Button text sits lower in Safari

The clearer the report, the faster it gets resolved.

---

## 💡 Feature Requests

Simplify.css intentionally avoids becoming a “CSS toolkit.”
That said, new ideas are always welcome if they meet these criteria:

- Solve **cross-browser inconsistency** or **accessibility issues**
- Improve **developer experience** or **readability**
- Stay within the **scope of foundation-level behavior**, not design choices

When proposing a feature:
- Explain *why* it matters
- Describe the technical reasoning or inconsistency it addresses
- Provide a minimal CSS example

**Avoid** feature requests that:
- Add visual opinions (colors, typography, shadows, spacing presets)
- Depend on frameworks, preprocessors, or external tools

---

## 🧩 Pull Requests

Simplify.css values small, precise, well-documented contributions.

### 1. Fork & Clone
```bash
git clone https://github.com/mouryaabhay/simplify.css
cd simplify.css
git remote add upstream https://github.com/abhay-mourya/simplify.css
````

### 2. Sync Latest Code

```bash
git checkout main
git pull upstream main
```

### 3. Create a Branch

```bash
git checkout -b <topic-branch-name>
```

### 4. Make Focused Commits

* Keep each commit atomic and descriptive.
* Use conventional commit messages:

```
fix: correct baseline alignment for <button> in Safari
chore: update comment structure for input states
docs: clarify contributing section
```

### 5. Test Before Submitting

* Open the included test HTML file or create a new sandbox to verify the behavior.
* Test on at least Chrome, Firefox, and Safari.

### 6. Submit Your Pull Request

Push to your fork and open a PR with:

* A concise title
* A clear description of what changed and why
* Any relevant test notes or references

---

## 🎨 CSS Style Guide

To keep Simplify.css consistent, follow these conventions:

| Rule                                    | Description                                                                    |
| --------------------------------------- | ------------------------------------------------------------------------------ |
| **Order logically**                     | From universal rules → HTML elements → form controls → states/pseudo-elements. |
| **Comment for intent**                  | Explain *why* a property exists, not *what* it does.                           |
| **Readable spacing**                    | Use one empty line between logical sections.                                   |
| **Use lowercase, hyphenated selectors** | e.g. `html`, `button:disabled`.                                                |
| **Avoid vendor prefixes**               | Except where browser-critical and verified.                                    |
| **Maintain neutral behavior**           | Do not visually restyle; only correct inconsistencies.                         |
| **1rem = 10px scale**                   | Keep measurements simple and proportionate.                                    |

**Example of acceptable commenting:**

```css
button:disabled {
  cursor: default; /* Keeps disabled buttons visually non-interactive */
}
```

---

## 🧩 Testing Philosophy

Simplify.css doesn’t use automated CSS tests yet — visual consistency is verified manually.

When testing:

* Use multiple browsers (Chrome, Firefox, Safari, Edge)
* Check different zoom levels and system fonts
* Validate accessibility (focus rings, scaling)

If you notice cross-browser rendering drift, isolate the root cause before proposing fixes.

---

## 🧰 Maintainer Guidelines

If you have write access or maintain a fork:

1. Ensure all PRs align with Simplify.css principles.
2. Avoid adding aesthetic or framework-specific styles.
3. Squash minor commits for clarity.
4. Tag new releases following **Semantic Versioning**.

---

## 🧮 Versioning Policy

Simplify.css follows [Semantic Versioning (SemVer)](https://semver.org/):

| Type      | Version | When Used                                                |
| --------- | ------- | -------------------------------------------------------- |
| **MAJOR** | `2.0.0` | When breaking rendering behavior or browser expectations |
| **MINOR** | `1.1.0` | When adding new stable, backward-compatible defaults     |
| **PATCH** | `1.0.1` | For fixes, typos, or documentation updates               |

All CSS rule changes are considered **MAJOR**, since even a one-line edit can alter visual rendering.

---

## 🧾 Code of Conduct

Please maintain a respectful, professional tone in all discussions.
We welcome developers of all backgrounds — the goal is to make the web more consistent, not competitive.

* Be constructive.
* Keep discussions technical.
* Credit others’ findings and observations.

Trolling, personal attacks, or dismissive comments will not be tolerated.

---

## ❤️ Acknowledgment

Simplify.css exists to **stabilize the unpredictable**, not to replace other tools.
It’s made possible by the shared curiosity, patience, and attention to detail of contributors like you.

> “Good CSS doesn’t shout — it balances.”
> *— simplify.css philosophy*
