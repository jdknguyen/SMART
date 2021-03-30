# SMART (Semi-Manual Alignment to Reference Templates)

**Pre-print: [SMART: An open source extension of WholeBrain for iDISCO+ LSFM intact mouse brain registration and segmentation](https://www.biorxiv.org/content/10.1101/727529v1)**

## Mar-30-2021: SMART version 1.1 release

It's been a few years since the initial release of [SMART](https://github.com/mjin1812/SMART), and we have a few updates. First off, we've moved the repository here! We've also implemented some bug fixes and new features.

The first set of new features allows users to 

To do this, we've added three functions: `concatenate()`, 

### New Features
- Duplicate cleanup bug fix
- Forward warp bug fix
- Function to count segmented cells before and after duplicate cleanup - `cell_counter()`
- Concatenation function to merge multiple datasets
- Function to compile cell counts from multiple datasets into one document
- Function to calculate group data from multiple datasets
- Voxelization function to allow users to run a voxel-based analysis, in addition to SMART's conventional region-based analysis, and generate cell density heatmaps
- Function to run statistical tests on voxelized datasets

## What is SMART?

Mapping immediate early gene (IEG) expression across intact brains is becoming a popular approach for identifying the brain-wide activity patterns underlying behavior. Registering whole brains to an anatomical atlas presents a technical challenge that has predominantly been tackled using automated voxel-based registration methods; however, these methods may fail when brains are damaged or only partially imaged, can be challenging to correct, and require substantial computational power. Here we present an open source package in R called SMART (semi-manual alignment to reference templates) as an extension to the WholeBrain framework for automated segmentation and semi-automated registration of experimental images to vectorized atlas plates from the Allen Brain Institute Mouse Common Coordinate Framework (CCF).

The SMART package was created with the novice programmer in mind and introduces a streamlined pipeline for aligning, registering, and segmenting large LSFM volumetric datasets with the CCF across the anterior-posterior axis, using a simple ‘choice game’ and interactive user-friendly menus. SMART further provides the flexibility to register partial brains or discrete user-chosen experimental images across the CCF, making it compatible with analysis of traditionally sectioned coronal brain slices. 

## Pipeline 👷
![](docs/schematics/pipeline_schematic.PNG)

## Installation ⚙️

- [Install SMART](docs/installation.md)

## Tutorial 📚
- [Introduction](docs/index.md) 🔨
- [Full Tutorial](docs/tutorial.md) 🏭

## Resources 💾

### Wholebrain webpage
- [Wholebrain by Daniel Furth](https:/http://www.wholebrainsoftware.org/) 🐭

### Open brain map
- [Interactive open brain map](https://http://www.openbrainmap.org/#2/7345/5135) 🗺️

### SMART example data and references
- [Access sample data here](docs/example_data.html) 📘

### Golden Lab webpage
- [Sam Golden Lab UW](https://goldenneurolab.com/) 🧪🧫🐁

## License 📃
[insert license info?]

## Contributors 🤼
- [Michelle Jin](https://github.com/mjin1812)
- [Joseph Nguyen](https://github.com/jdknguyen)
- Rajtarun Madangopal
