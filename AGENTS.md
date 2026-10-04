# Repository Guide

## Purpose
This repository contains Elyk's GitHub profile README. `README.md` presents the profile, achievements, portfolio link, skills, and an animated photo slideshow. It is a content-focused repository with no application code or automated test suite.

## Profile content
- Keep the README's opening order: slideshow, achievements, name and role, then the rest of the profile.
- Preserve achievement names, rankings, and divisions as supplied by the user. Do not infer or expand event names.
- Use repository-relative paths for local README images and retain descriptive alt text.

## Photo slideshow
- `assets/rstw-slideshow.gif` is the generated slideshow embedded in the README. Keep it at 600×450 and display it at 600 pixels wide.
- Build slides from image assets in `assets/`, excluding generated GIFs. Keep this order: `rstw-finalist-edit.jpg`, `rstw-panel.png`, `rstw-article.jpeg`, `runner up.jpeg`, `rstw-solo.jpg`, `rsc.jpg`, `DELFIN_DWIA_AWARD.jpg`, `soma-champs.jpg`, `Tabang-Finalist.jpg`. Append newly added images alphabetically after these.
- Preserve source images. Apply no color filter or tone adjustment. Fit the complete image inside the frame without cropping or stretching. For aspect-ratio differences, fill the frame with a softly blurred, enlarged copy of that same photo behind the full-size fitted original; avoid blank or white padding.
- Hold each slide for about 2.5 seconds, crossfade to the next over about 0.5 seconds, and loop continuously, including the final-to-first transition.
- When an image is added, removed, or replaced, regenerate the GIF in the same change and verify that it reflects the current assets and ordering.

## Validation
- Confirm the README references `assets/rstw-slideshow.gif` exactly once and the GIF decodes with the expected images in order, dimensions, transitions, and infinite loop.
- Run `git diff --check`. There are no application tests in this repository; use asset and README validation for slideshow changes.
