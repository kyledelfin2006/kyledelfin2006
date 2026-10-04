# README Slideshow Implementation Plan

## Goal
Replace the README image grid with one looping slideshow built from the images in `assets/`.

## Slide order
1. `rstw-finalist-edit.jpg`
2. `rstw-panel.png`
3. `rstw-article.jpeg`
4. `rstw-solo.jpg`
5. Remaining assets alphabetically: `DELFIN_DWIA_AWARD.jpg`, `rsc.jpg`, `rstw-poultri.jpg`, `soma-champs.jpg`, `Tabang-Finalist.jpg`.

## Implementation
- Preserve all original images and apply no filter, tint, brightness, contrast, or saturation adjustments.
- Fit every image, without cropping, into a fixed 1600×1200 frame with neutral padding; display the GIF at 800 pixels wide in the README for sharper rendering.
- Generate `assets/rstw-slideshow.gif` with each slide displayed for 3 seconds and continuous looping.
- Replace the README grid with one centered image referencing the GIF.
- Remove only the redundant generated copies in `assets/filtered/`.

## Acceptance checks
- Verify all nine GIF frames and their order, 3000 ms timing, and infinite looping.
- Inspect the frames for consistent sizing and preserved image content; check the optimized GIF size.
- Confirm the README references the GIF exactly once, the file exists, and `git diff --check` passes.
