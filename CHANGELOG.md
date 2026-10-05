# Changelog

## v1.0.2 (2026-09-28)

Windows executable. The user manual is still not included (draft only). Help → User Manual looks for `docs/PLS_User_Manual.pdf` beside the program. Public build engines are unchanged: DeLTA and SIGMA only (no CONTIN / POSFIT).
### PALStudio
- The physical-variable window is the same shared dialog as DBStudio (nth-number spinner, sequence, and pattern extract).
- The first batch window shows the restored file list, can add files from more than one folder, and marks each file fitted, new, or missing.
- Already-fitted files are skipped unless Refit files that already have results is checked. With chaining on, the first new file starts from the last kept fit.
- Bug fixed: after fitting only the new files, choosing an old file in the main-window list showed the SIGMA curve and dropped the spectrum and the DeLTA fit.
- Bug fixed: A PALStudio batch window and a DBStudio batch window can both stay open. One no longer steals the click from the other.

### CDBStudio
- Auto-align / drift: 2D background is fitted once on the full matrix; slices only realign `Project(M)`. The same `B` is subtracted after recombination (no per-slice scaling of `B` by slice/full counts).
- 1D momentum spectra keep signed residuals: `Project(M) − Project(B)` with no clip-to-zero after recombination. Clipping negatives used to bias high-momentum ratio curves when a low-count spectrum was clipped more than a high-count one.
- Adaptive rebinning / smoothing on ratio curves is view-only; the archival pointwise ratio stays on the original 1D grid.
- Ratio export and display paths use the signed residual consistently (error bars stay non-negative magnitudes).

### Suite
- Plot Save as SVG/PDF: toolbar preloads matplotlib backends so Save works after 2D debug plots that use the Agg canvas.
- README screenshots for the hub and each Studio (already on the docs branch; tied to this release).
- README / changelog clarify that the public Windows build ships DeLTA and SIGMA only.

### Packaging
- Release zip is the frozen `PLS2026` folder only (`PLS2026.exe` + `_internal`). Source `.py` files are not included. CONTIN / POSFIT binaries are omitted from the public zip.

## v1.0.1 (2026-09-10)

Windows executable. The user manual is not included (still in draft). Help → User Manual looks for `docs/PLS_User_Manual.pdf` beside the program; that file will be added in a later release. The public build does not include the legacy Fortran CONTIN or POSFIT (PFPOSFIT) engines; PALStudio discrete and continuum analysis use DeLTA and SIGMA.

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
