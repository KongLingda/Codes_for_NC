# Codes_for_NC

Core codes for readers to reproduce or inspect the plotting workflows used for the figures in the manuscript.

## Important note on local paths

Before running these notebooks, please modify the input and output paths to match your own local directory structure.

Some notebooks still contain example paths from the authors' local working environment, for example paths under external disks or local data folders. These paths are only placeholders showing where the intermediate products were stored during the analysis. They will not work on another computer unless they are replaced by paths to the corresponding files on that computer.

In practice, readers should first search each notebook for path definitions or file-loading commands, such as:

- `path = ...`
- `pd.read_csv(...)`
- `fits.open(...)`
- `np.load(...)`
- `plt.savefig(...)`
- any absolute path beginning with `/Users/`, `/Volumes/`, `/home/`, or another machine-specific directory

and then replace them with the correct local paths.

## What is included

This repository contains notebooks used to generate or assist with generating figures in the paper, including plotting scripts and analysis/visualization workflows based on public Python packages such as `Stingray` and `VmdTransformer`.

## What is not included

This repository does not include the preliminary Insight-HXMT data reduction scripts.

The original observational data are public and can be downloaded from the Insight-HXMT archive:

http://archive.hxmt.cn/proposal

Spectral analysis and phase-resolved spectral analysis can be performed with the officially recommended Insight-HXMT data analysis software, `hpipeline`.

## Intermediate data products

Some notebooks require intermediate products such as QDP files, FITS files, MCMC chains, phase-resolved spectra, or processed light curves. These files may need to be generated from the public Insight-HXMT data using the standard Insight-HXMT analysis tools, or requested from the corresponding authors as described in the paper's Data availability statement.

## Typical Python dependencies

The notebooks may require packages such as:

- `numpy`
- `scipy`
- `pandas`
- `matplotlib`
- `astropy`
- `stingray`
- `sktime`
- `corner`
- `scikit-learn`
- `Pillow`
- `PyMuPDF`

Depending on the notebook, additional packages may be required.

## Suggested workflow

1. Download the public Insight-HXMT data from the archive.
2. Process the data with the official Insight-HXMT tools, including `hpipeline`, where appropriate.
3. Prepare the required intermediate files, such as spectra, QDP files, FITS files, or MCMC chains.
4. Open the relevant notebook.
5. Modify all local file paths to point to your own data and output directories.
6. Run the notebook cells to reproduce or inspect the figure-generation workflow.
