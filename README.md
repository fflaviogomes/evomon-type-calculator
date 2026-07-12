# Evomon Dual-Way Type Effectiveness Calculator

## Overview
This is a lightweight HTML/JavaScript calculator for Evomon-style battle type matchups. It computes both:

- **Defense**: how much damage the selected dual type takes from each attacker type
- **Offense**: which opponent types are best hit by your active types

The UI includes a direct reference link to the Evomon wiki:
- https://evomon.wiki/type-chart

## Files
- `Evomon-Type-Calculator.html` — main calculator page with built-in type data and result panels.
- `Evomon-Type-Calculator-README.md` — this documentation file.

## How to Use
1. Open `Evomon-Type-Calculator.html` in a browser.
2. Select a primary type from the first dropdown.
3. Select a secondary type from the second dropdown, or choose `None (Pure Type)`.
4. The page automatically updates:
   - left panel shows incoming damage multipliers
   - right panel shows offense matchups and best active type for each opponent

## Code Structure
- `typeDB` stores type metadata:
  - `color` for badge styling
  - `icon` emoji for display
  - `effectiveness` mapping against target types
- UI is generated dynamically from `typeDB`.
- `calculateAll()` recomputes defense and offense whenever the selected types change.
- `displaySection()` renders result rows and badges.

## Notes and Suggestions
- The current type list includes a standard Evomon subset, but you can extend `typeDB` with more types or custom effectiveness values.
- `type2` supports `None` for pure-type matchups.
- Offense calculations choose the stronger of the two selected types when evaluating dual-type targets.

## Evomon Link
For more Evomon battle design details and reference, visit:
- https://evomon.wiki
