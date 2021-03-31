# Tutorial

## Pipeline breakdown:

For processing a wholebrain dataset, the pipeline is split into 6 sections. These sections are listed below along with the functions that belong to each section:

**Part 1: Setup pipeline**

  - [`setup_pl()`](id#1) User friendly way to setup parameters for whole
    or partial brain pipeline analysis.
  - `im_sort()` A function to sort image paths for imaging
    datasets.
  - `get_savepaths()` Generate savepaths and save directories.

**Part 2: Alignment (W)**

  - `choice()` **(W)** User friendly choice game to align
    internal reference atlas plates.
  - `brainmorph()` **(W)** Generate a brain morph plot.
  - `interpolate()` **(W)** Interpolate all AP and z numbers for
    atlas plates in a whole brain project

**Part 3: Registration**

  - `registration2()` Console user interface built on top of
    registration() function from the wholebrain package.
  - `regi_loop()` Automatically loops through the image
    registration process for the imaging dataset.

**Part 4: Segmentation, duplicate cleanup, & forward warping**

  - `filter_loop()` Loops through reference slices and allows
    user to check/change filter settings for segmentation or
    registration.
  - `seg_loop()` Loop through and segments images in the
    segmentation channel.
  - `clean_duplicates()` **(W)** Duplicate cell count clean up
    of segmentation output.
  - `cell_counter()` Determines total number of cells
    segmented, retained, and removed by duplicate cleanup.
  - `forward_warp()` Performs forward warp loop back onto atlas
    space using segmentation and registration output.

**Part 5. Dataset manipulation and plotting**

  - `isolated_dataset()` Isolates a user-specified subset of
    the forward warped dataset.
  - `get_rois()` Gets a subset of the forward warped dataframe
    of just regions of interest.
  - `get_sunburst()` Generates a sunburst plot using a forward
    warped dataset.
  - `get_tree()` Creates a dataframe of hierarchical region
    cell count data.
  - `glassbrain2()` Generates a 3D plot of cells counts with
    option of removing glassbrain in the background.
  - `get_table()` Generates a dataframe showing region
    acronyms, their full name, hierachical paths, total cell counts,
    left and right counts, and cell count percentages.

**Part 6. Aggregating data from multiple analyses**

  - `concatenate()` Combines datasets from multiple brains.
  - `cell_count_compilation()` Compiles cell counts from
    multiple brains.
  - `get_groups()` Compiles group data from individual brains.
  - `voxelize()` Generate voxel-based heatmaps from multiple
    brains.
  - `voxel_stats()` Run statistical tests on voxel-based
    heatmaps.

Below is a walkthrough of each of these functions and the pipeline as a whole using an example whole brain dataset.

## Part 1: Setup pipeline ##

This sections sets up analysis parameters, sorted image paths, and generates savepaths and directories for the rest of the pipeline.

**Step 1.**

`setup_pl()`(id#1) This function asks the user for setup information. Based on input from the user, the function returns a list of parameters for either a whole or partial brain analysis.

```diff
# Scroll to the details section of the help page to see the setup parameters
?setup_pl()

# Run setup_pl, enter parameter information to the console, 
# and store the output list into a variable named setup

setup <- setup_pl()

# Check or modify your setup parameters 
setup <- setup_pl(setup)

# Note: Whenever a different user works on analyzing the same dataset,
# run the above command to change user initials. This will keep track of
# who did what. 
```

### Tips: When providing folder paths, do not put quotes around the path to the console input.











