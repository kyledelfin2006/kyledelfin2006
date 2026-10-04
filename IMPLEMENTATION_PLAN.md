# README Image Gallery Implementation Plan

## Goal
Replace the remote README hero image with a complete, consistently treated gallery sourced from `assets/`.

## Ordered gallery
1. `rstw-finalist-edit.jpg`
2. `rstw-panel.png`
3. `rstw-article.jpeg`
4. `rstw-solo.jpg`
5. Remaining assets alphabetically: `DELFIN_DWIA_AWARD.jpg`, `rsc.jpg`, `rstw-poultri.jpg`, `soma-champs.jpg`, `Tabang-Finalist.jpg`.

## Implementation
- Preserve source images and generate treated copies in a dedicated assets subfolder.
- Apply one subtle natural-color adjustment consistently to each copy.
- Update README to display all nine treated copies in the listed order in a two-column HTML table with descriptive alt text and consistent display sizing.

## Acceptance checks
- All nine expected image files are referenced exactly once and in order.
- Every referenced path resolves to a generated copy; originals remain intact.
- Inspect the rendered README for ordering, sizing, and a balanced gallery layout.
