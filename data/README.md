This directory contains local datasets required to run the project.

The following files are NOT included in the repository:
- `metadata.csv`
- `images/`
- `whoi_plankton_raw/`

To recreate the dataset:
1. Download WHOI-Plankton images using the provided R script
2. Filter phytoplankton classes
3. Generate `metadata.csv` using `scripts/build_metadata.py`