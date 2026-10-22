# Pt(111) ORR Literature Dataset

Cyclic voltammograms and ORR polarization curves for Pt(111) in 0.1 M HClO₄, digitized from published figures.

**[Open the interactive data viewer →](https://cs3833.github.io/Pt-111-in-0.1M-HClO4-Database/)**

The viewer plots and compares the datasets, with filters, exclusion criteria, normalization options and CSV export.

## Contents

- `CV_Data/`: extracted cyclic voltammograms as CSV files
- `Pol_Curve_Data/`: extracted ORR polarization curves as CSV files
- `metadata.csv`: source citation, DOI, and experimental conditions for each dataset
- `index.html`: the data viewer
- `viewer_data.json`: compact copy of all curves that lets the viewer load quickly

## Numbering scheme

Each row in `metadata.csv` is identified by a `ds_key` of the form `N-P`. `N` is the dataset number, one per source publication. `P` numbers each unique polarization curve scan from that publication, such as scans at different rotation rates. A dataset with no polarization curve, or with only one, has the default suffix `-1`.

Data files are named from the same key:
- `CVN.csv` is the CV for dataset `N`. One CV is shared by all polarization curve scans from that publication.
- `PolCurveN-P.csv` is the polarization curve for `ds_key` `N-P`. When a publication has only one polarization curve, the file is named `PolCurveN.csv`.

For example, `CV18.csv` together with `PolCurve18-1.csv`, `PolCurve18-2.csv` and `PolCurve18-3.csv` are the data for `ds_key` 18-1, 18-2 and 18-3.

Data were extracted with [Bulk-Figure-Data-Extraction](https://github.com/cs3833/Bulk-Figure-Data-Extraction).

Please cite the original publications listed in `metadata.csv` when using these datasets.
