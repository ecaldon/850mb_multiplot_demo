# 850mb_multiplot
An easily customizable notebook to create a multi-subplot figure with 850mb temperature and wind RAP analysis, Multi-Radar Multi-Sensor (MRMS) products, and even lightning mapping array points.

This notebook was created as part of the Lake-Effect Electrification (LEE) Project to easily plot salient data points from key LES events during the field campaign.

## How to get started...
Create and activate the conda environment on your machine using the environment.yml file.
```
conda env create -f environment.yml
conda activate 850mb_multiplot
```
Next, download the `850mb_multipanel_demo.ipynb` file (and files in the `rap` directory for some RAP files to immediately play with) into a convenient directory on your machine. `cd` to this directory in your terminal and then run
```
conda activate 850mb_multiplot
jupyter lab
```
You should be ready to run the notebook in your newly created environment! Go through the customization blocks to change the directories and settings to your specifications. Happy plotting!

## Recent updates...
**Major Update 7/16/25**
- New capability to use NSSL's Multi-Radar Multi-Sensor (MRMS) products as a layer, replacing the need for gridded NEXRAD files, including the following new customizations:
  - Ability to choose fields from over 200 MRMS products
  - A gate filter to mask data under a certain user-defined minimum
- Improved Markdown comments in the notebook for easier navigation
- Added figure DPI customizations to designated customization code blocks
- Added toggle function to save figure, allowing for faster debugging and customization since saving the figure takes about 2 minutes with a DPI of 500 and six subplots
- Back-end changes and bug fixes:
  - Changed RAP code to use `cfgrib` module instead of `pygrib` to allow for MRMS and RAP products to work efficiently and properly
  - Improved RAP caching so that RAP analysis plotting only uses cached files that have the same data area as the currently-defined area
  - `lma` directory automatically created, preventing path errors
