# Positron Lab Suite (PLS2026)

Windows desktop software for positron annihilation spectroscopy (PAS) data analysis.

This repository distributes a **compiled Windows executable**. Source code is not included; it is available from the author on request.

**Download:** [latest Release](https://github.com/fluidlight/pls/releases/latest)

## Modules

The central hub launches four analysis modules:

| Module | Purpose |
|---|---|
| **PALStudio** | Positron annihilation lifetime spectroscopy (PALS). Discrete multi-exponential fitting (DeLTA) and continuum lifetime distributions (SIGMA / CONTIN). |
| **DBStudio** | Doppler broadening spectroscopy (DBS). Energy calibration, background subtraction, and *S*/*W* parameter extraction, including batch and live monitoring. |
| **CDBStudio** | Coincidence Doppler broadening (CDBS). List-mode / matrix processing, 1D momentum projections, and elemental fingerprint ratio curves. |
| **VEPStudio** | Variable-energy positron (VEP) depth profiling. Drift–diffusion fitting of *S*(*E*) / *W*(*E*), with a built-in multilayer simulator. |

Shared tools include a multi-spectrum data hub, source-component estimator, *S*–*W* correlation analyzer, and project save/restore across modules.

## Requirements

- Windows 10 or 11, 64-bit
- No Python installation is required
- A few GB of free disk space (the unpacked build is about 0.7 GB)

## Install and run

1. From [Releases](https://github.com/fluidlight/pls/releases), download `PLS2026-v1.0.0-windows.zip`.
2. Unzip the archive to a local folder (for example `C:\PLS2026`). Do not run the program from inside the zip file.
3. Open the unzipped `PLS2026` folder and double-click **`PLS2026.exe`**.

Keep **`PLS2026.exe`** and the **`_internal`** folder together. Moving only the `.exe` will break the program.

Windows SmartScreen or antivirus software may warn about an unsigned PyInstaller build. If you downloaded this zip from the official Release page, choose **More info → Run anyway**. Adding an exclusion for the unzipped folder avoids repeated scans.

## Citation

If you use Positron Lab Suite in published work, please cite the accompanying paper:

> M. Liu, *Positron Lab Suite: A comprehensive software suite for integrated positron annihilation spectroscopy data analysis*, (2026). *[journal / DOI to be added]*

A `CITATION.cff` file is included in this repository.

## License and source

Copyright © 2026 Ming Liu, North Carolina State University. All rights reserved.

The Windows executable is provided for academic and non-commercial research use. See [LICENSE](LICENSE) for terms. Source code is not hosted here; contact the author if you need it.

## Contact

Ming Liu  
Department of Nuclear Engineering, North Carolina State University  
mliu4@ncsu.edu
