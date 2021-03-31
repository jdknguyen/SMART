# Tutorial

## Pipeline breakdown:

For processing a wholebrain dataset, the pipeline is split into 5 sections. These sections are listed below along with the functions that belong to each section:

**Part 1: Setup pipeline**

  - `setup_pl()` User friendly way to setup parameters for whole
    or partial brain pipeline analysis.
  - [`im_sort()`](#id2) A function to sort image paths for imaging
    datasets.
  - [`get_savepaths()`](#id3) Generate savepaths and save directories.

**Part 2: Alignment (W)**

  - [`choice()`](#id4) **(W)** User friendly choice game to align
    internal reference atlas plates.
  - [`brainmorph()`](#id5) **(W)** Generate a brain morph plot.
  - [`interpolate()`](#id6)**(W)** Interpolate all AP and z numbers for
    atlas plates in a whole brain project

**Part 3: Registration**

  - [`registration2()`](#id7) Console user interface built on top of
    registration() function from the wholebrain package.
  - [`regi_loop()`](#id8) Automatically loops through the image
    registration process for the imaging dataset.

**Part 4: Segmentation, duplicate cleanup, & forward warping**

  - [`filter_loop()`](#id9) Loops through reference slices and allows
    user to check/change filter settings for segmentation or
    registration.
  - [`seg_loop()`](#id10) Loop through and segments images in the
    segmentation channel.
  - [`clean_duplicates()`](#id11) **(W)** Duplicate cell count clean up
    of segmentation output.
  - [`cell_counter()`](#id12) Determines total number of cells
    segmented, retained, and removed by duplicate cleanup.
  - [`forward_warp()`](#id13) Performs forward warp loop back onto atlas
    space using segmentation and registration output.

**Part 5. Dataset manipulation and plotting**

  - [`isolated_dataset()`](#id14) Isolates a user-specified subset of
    the forward warped dataset.
  - [`get_rois()`](#id15) Gets a subset of the forward warped dataframe
    of just regions of interest.
  - [`get_sunburst()`](#id16) Generates a sunburst plot using a forward
    warped dataset.
  - [`get_tree()`](#id17) Creates a dataframe of hierarchical region
    cell count data.
  - [`glassbrain2()`](#id18) Generates a 3D plot of cells counts with
    option of removing glassbrain in the background.
  - [`get_table()`](#id19) Generates a dataframe showing region
    acronyms, their full name, hierachical paths, total cell counts,
    left and right counts, and cell count percentages.

**Part 6. Aggregating data from multiple analyses**

  - [`concatenate()`](#id20) Combines datasets from multiple brains.
  - [`cell_count_compilation()`](#id21) Compiles cell counts from
    multiple brains.
  - [`get_groups()`](#id22) Compiles group data from individual brains.
  - [`voxelize()`](#id23) Generate voxel-based heatmaps from multiple
    brains.
  - [`voxel_stats()`](#id24) Run statistical tests on voxel-based
    heatmaps.
