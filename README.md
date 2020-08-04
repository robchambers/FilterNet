
# FilterNet: A many-to-many deep learning architecture for time series classification

[![DOI](https://zenodo.org/badge/242397153.svg)](https://zenodo.org/badge/latestdoi/242397153)

This repository contains code to reproduce the results and figures in the paper: 
*[FilterNet: A many-to-many deep learning architecture for time series classification](https://www.mdpi.com/703084)*.

## Setup
The easiest way to run this software is via the Anaconda Python distribution.

1. Install Anaconda
2. Run `conda env create -f environment.yaml`
3. Enable the `filternet` environment, like, `source activate filternet`
4. Install filternet so it is importable, by running `pip install -e .` in the same 
   directory as setup.py

## Running tests
In the root dir of this repo:

```
pytest tests
```

This will be *really* slow the first time because it has to download and pre-process 
several large AR datasets.

Subsequent test runs will probably still be slow, but... less slow.

## Reproducing Results

1. Run the scripts in the `scripts/` directory. These are very long-running scripts that 
   reproduce each experimental condition many times. You might want to set, e.g., `NUM_REPEATS=1` 
   if you don't need this level of reproducibility.
   
2. Run the notebooks to re-produce the figures. You might need to edit a few paths to specific
   models to match the filenames on your system, especially if you changed the 
   `NAME` or `NUM_REPEATS` parameters.
     
------
Copyright (C) 2020 Pet Insight  Project - All Rights Reserved
