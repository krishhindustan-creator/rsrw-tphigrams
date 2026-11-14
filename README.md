# IMD RS/RW T-phi grams

**T-phi grams and 39 thermodynamic indices for every IMD radiosonde/radiowind (RS/RW) station that reported, updated automatically.**

Live page: https://krishhindustan-creator.github.io/rsrw-tphigrams/
Companion site (cyclone, district and subdivisional guidance): https://krishhindustan-creator.github.io/cyclone-nwp/

> Guidance products prepared at RWFC New Delhi, India Meteorological Department. Not official IMD forecasts.

## What the page gives

- A T-phi gram for each ascent: temperature and dew-point profiles, the parcel path with CAPE shaded red and CIN blue, wind barbs and a hodograph.
- An index sheet of 39 values per station, including surface-based, mixed-layer and most-unstable CAPE; CIN; LCL, LFC and EL; lifted and Showalter indices; K index; total totals; SWEAT; precipitable water; DCAPE; bulk shear and storm-relative helicity; SCP and STP; wet-bulb zero and freezing levels.
- Quality flags: values outside physical limits (e.g. CAPE above 7000 J/kg, precipitable water outside 2-90 mm) are flagged on the sheet, not hidden.
- Two views: all stations for one ascent, or one station for all dates; filter by station name.

## Data and updates

- Source: IMD CLIMS RS/RW data (File-3 standard summary, or File-4 when File-3 is missing). About 45 stations report at a typical 00 UTC ascent.
- Updated at 07:30 and 09:00 IST (00 UTC ascents) and 19:30 and 21:00 IST (12 UTC); the later run adds stations that report late.
- Rolling archive of all ascents in `charts/YYYYMMDD_HHZ/`.

## How it is made

This repository holds only the published page (`index.html`, `archive.js`, `charts/`). The page is rebuilt by `rsrw_tphigrams.py`, which runs on a schedule in GitHub Actions in the [cyclone-nwp](https://github.com/krishhindustan-creator/cyclone-nwp) repository (workflow `.github/workflows/tphi.yml`). CLIMS access uses institutional credentials held as an encrypted secret; only derived charts are published.

All code was written by a generative AI assistant (Claude, Anthropic) from requirements set, tested and validated by the forecaster. The system is described in: Mishra, K., Kumar, V. *Building zero-cost operational weather decision support with a generative AI coding assistant: an Indian case study.* Manuscript in preparation.

## Licence and contact

Code: [MIT License](LICENSE). RS/RW data remain under IMD's data policy.

Krishna Mishra, Scientist D, Regional Weather Forecasting Centre, New Delhi, India Meteorological Department - krishhindustan@gmail.com - ORCID 0000-0003-3028-7383
