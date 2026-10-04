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
- Preserve all original images and apply one subtle natural-color treatment to each slide.
- Fit every image, without cropping, into a fixed 800×600 frame with neutral padding.
- Generate `assets/rstw-slideshow.gif` with each slide displayed for 3 seconds and continuous looping.
- Replace the README grid with one centered image referencing the GIF.
- Remove only the redundant generated copies in `assets/filtered/`.

## Acceptance checks
- Verify all nine GIF frames and their order, 3000 ms timing, and infinite looping.
- Inspect the frames for consistent sizing and preserved image content; check the optimized GIF size.
- Confirm the README references the GIF exactly once, the file exists, and `git diff --check` passes.
