# 850mb_multiplot
An easily customizable notebook to create a multi-subplot figure with 850mb temperature and wind RAP analysis, NWS radar, and even lightning mapping array points.

This notebook was created as part of the Lake-Effect Electrification (LEE) Project to easily plot salient data points from key LES events during the field campaign.

## How to get started...
Install the environment.yml file, and create and activate the conda environment on your machine. Then, install the other modules that do not play nice with the conda environment.
```
conda env create -f environment.yml
conda activate 850mb_multiplot
pip install arm_pyart
pip install nexradaws
```
Then, you should be ready to run the notebook in your newly created environment! Happy plotting!
