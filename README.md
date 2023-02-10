 ## Instructions for running DiffImpact
 1. Install and initialize [Anaconda3](https://docs.anaconda.com/anaconda/install/linux/)
 2. Clone the `diffimpact` repo from this page.
 3. In the Anaconda `base` environment, change the working directory to this repo's folder and install the conda env with
```
cd diffimpact
conda env create -f diffimpactenv.yml
```
 4. From within the `diffimpact` directory, initialize and update the submodule for our ddsp fork with
 ```
 git submodule init
 git submodule update
```
 5. Go to our DDSP fork with and install it in the pip environment with
 ```
 cd ddsp
 pip install -e .
 cd ../
 ```
 6. Install the conda environment as kernel to Jupyter notebooks with
  ```
  python -m ipykernel install --user --name=diffimpactenv
 ```
 7. Run 
 ```
 jupyter notebook
 ```
 8. Make sure each Jupyter notebook is set to the `diffimpactenv` kernel before running code 
 9. See `AnalysisBySynthesis.ipynb` and `SourceSeparation.ipynb` for the analysis by synthesis experiment and the source separation experiment, respectively.

### Paper
Please check out our paper, ["DiffImpact: Differentiable Rendering and Identification of Impact Sounds"](https://openreview.net/forum?id=wVIqlSqKu2D), published at the Conference on Robot Learning (CoRL), 2021.

If you use this code, please cite us:
  ```
  @inproceedings{clarke2022diffimpact,
	  title={Diffimpact: Differentiable rendering and identification of impact sounds},
	  author={Clarke, Samuel and Heravi, Negin and Rau, Mark and Gao, Ruohan and Wu, Jiajun and James, Doug and Bohg, Jeannette},
	  booktitle={Conference on Robot Learning},
	  pages={662--673},
	  year={2022},
	  organization={PMLR}
}
```