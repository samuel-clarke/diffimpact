 ## Instructions for running DiffImpact
 1. Install and initialize [Anaconda3](https://docs.anaconda.com/anaconda/install/linux/)
 2. Clone the `diffimpact` repo from this page.
 3. In the Anaconda `base` environment, change the working directory to this repo's folder and install the conda env with
`cd diffimpact`
`conda env create -f diffimpactenv.yml`
  
 5. From within the `diffimpact` directory, initialize and update the submodule for our ddsp fork with
 `git submodule init`
 `git submodule update`
 6. Go to our DDSP fork with and install it in the pip environment with
 `cd ddsp`
 `pip install -e .`
 `cd ../`
 8. Install the conda environment as kernel to Jupyter notebooks with
  `python -m ipykernel install --user --name=diffimpactenv`
 9. Run `jupyter notebook`
 10. Make sure each Jupyter notebook is set to the `diffimpactenv` kernel before running code 
 11. See `AnalysisBySynthesis.ipynb` and `SourceSeparation.ipynb` for the analysis by synthesis experiment and the source separation experiment, respectively.