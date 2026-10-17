# East Timor language regions

Binary classification dataset used in GPSS / GPy lab notebooks for non-Gaussian likelihoods (expectation propagation).

## Contents

- `EastTimor2.pickle` — Python 2/3-compatible pickle containing `(X, y, polygons)`:
  - `X`: `(67, 2)` float64 lon/lat centroids
  - `y`: `(67, 1)` int64 binary labels (language region)
  - `polygons`: length-67 list of polygon vertex lists for map plots

## Provenance

- Historical download URL (now 403):
  `http://staffwww.dcs.shef.ac.uk/people/M.Zwiessele/gpss/lab2/EastTimor.pickle`
- Packaged for GPSS labs by Max Zwiessele; used in GPy crash-course / GPRS lab notebooks.
- MD5 of mirrored file: `16db10d067706fa3f03633408a8d201c`
- Identical copies found locally in:
  - `mlatcl/gpss/_notebooks/data/EastTimor2.pickle`
  - `SheffieldML/notebook/lab_classes/gprs/EastTimor2.pickle`
  - `lawrennd/mlprojects/gplvm/tex/oxford14/EastTimor2.pickle`

No generation script or upstream GIS sources were located in the teaching repos. Regenerating *de novo* would require recovering the original region/language map sources; until then this mirror preserves the teaching artifact as used historically.

## Intended consumer

`pods.datasets.east_timor` in [lawrennd/ods](https://github.com/lawrennd/ods) (backlog: `2026-10-17_east-timor-dataset`).
