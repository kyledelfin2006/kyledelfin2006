# README Slideshow Implementation Plan

## Goal
Replace the README image grid with one looping slideshow built from the images in `assets/`.

## Slide order
1. `rstw-finalist-edit.jpg`
2. `rstw-panel.png`
3. `rstw-article.jpeg`
4. `rstw-solo.jpg`
5. Remaining available images alphabetically: `DELFIN_DWIA_AWARD.jpg`, `rsc.jpg`, `runner up.jpeg`, `soma-champs.jpg`, `Tabang-Finalist.jpg`.

## Implementation
- Preserve all original images and apply no filter, tint, brightness, contrast, or saturation adjustments.
- Fill a fixed 800×600 frame edge to edge using a centered cover crop, without padding; display the GIF at 800 pixels wide in the README.
- Generate `assets/rstw-slideshow.gif` with each image held for 2.5 seconds, followed by a 0.5-second crossfade to the next image; loop continuously, including the final-to-first transition.
- Replace the README grid with one centered image referencing the GIF.
- Remove only the redundant generated copies in `assets/filtered/`.

## Acceptance checks
- Verify all nine source images appear in order, each 3-second interval includes a 2.5-second hold and 0.5-second crossfade, and the animation loops smoothly.
- Inspect the frames for edge-to-edge coverage and confirm the centered crops keep each subject legible; check the optimized GIF size.
- Confirm the README references the GIF exactly once, the file exists, and `git diff --check` passes.
