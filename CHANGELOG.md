# Changelog

## v1.0.1 (2026-09-10)

Windows executable. The user manual is not included (still in draft). Help → User Manual looks for `docs/PLS_User_Manual.pdf` beside the program; that file will be added in a later release.

### DBStudio
- After batch, pick any file from the main-window dropdown and re-analyze it (same idea as PALStudio).
- Bug fixed. Analyze Current Spectrum always fits the spectrum shown in the main window.
- S/W windows are anchored on the measured 511 keV peak channel, not on the linear-fit prediction (511 − b)/g.
- 511 keV is locked on by default; unlocking requires a warning. Enabling a third/fourth calibration peak warns that S is only comparable if every spectrum uses the same peak set.
- Batch Excel: FWHM monitor energy is in the column header; cells are the measured channel of that peak (drift vs Status flags).

### VEPStudio
- Recovery-test log: pass = green, check = orange, fail = red (per trial, not the whole block).
- Bug fixed: Recovery initial guesses are clipped to TRF bounds.
- Bug fixed: Simulator clears previous exclude-from-fit points; hover no longer crashes after a length mismatch.

### Suite
- Help → User Manual opens the same `docs/PLS_User_Manual.pdf` in every Studio (manual to be added).
- Plot Save includes SVG/PDF backends.

## v1.0.0 (2026-09-02)

First public Windows build on [GitHub Releases](https://github.com/fluidlight/pls/releases).
