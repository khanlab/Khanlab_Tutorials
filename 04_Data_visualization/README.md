# Khanlab Tutorial 4: Data visualization

## Objective:
Learn about a number of visualization tools and how to use them including ITKSnap, FSLeyes, Slicer, and Paraview!

## Prerequisites (Homework! Do this on your own before the tutorial):
* Download and install the latest version of [Paraview](https://www.paraview.org/) on your system
* Download and install the latest version of [3D Slicer](https://download.slicer.org/) on your system
* Download and install the latest version of [ITK-SNAP](http://www.itksnap.org/pmwiki/pmwiki.php?n=Downloads.SNAP3) on your system
* Download and install the latest version of [FSLeyes](https://users.fmrib.ox.ac.uk/~paulmc/fsleyes/userdoc/latest/install.html) on your system

## At the end of this tutorial, you will know:

### Paraview
* Visualize neuroimaging models & data on Paraview.
* Create multiple renderers to view / compare data
* Shortcuts & filters for manipulating loaded data
* View / create animations via paraview (great for visualizing tractography)

### 3D Slicer
* 

### ITK-SNAP
* How to load structural images and 3D segmentations (e.g., from Freesurfer)
* How to create NEW 3D segmentations using tools like free draw, active contour
* How to view and navigate segmentations in the 3D window

### FSL-Eyes
* How to load structural images and overlays
* How to optimize the view window (min/max intensity, greyscale/other)
* How to run FSL MELODIC ICA and load in FSLeyes to view noise/real components


## Tasks:

### Paraview
* Check on prerequisite (installation)
* Demo paraview
* Multiple render windows
* Animations

### 3D Slicer
* 

### ITK-SNAP
* Load T1 iamge, Load segmentation (Hippocampal?), view on 3 windows + 3D window
* Create new segmentatio: hippocampal. Dark band label, slice by slice (save segmentation), grow segmentation (save segmentation), load seg1 (darkband).

### FSL-Eyes
* Load T1 image, load overlay segmentation
* Run melodic ICA code.
* Save folder = melodic.ica
* load folder melodic.ica in melodic view
* view some noise and real components and make .txt to use for the filtering command


## Data:

### Paraview
* N/A

## Notes:
* Paraview can also perform other analyis (eg. finite-element modelling)

## Resources:
* Sharcnet Webinar on Paraview (2017): https://www.youtube.com/watch?v=yexB3W2FYM0
    * Good resource for learning about the extensive capabilities of paraview
* 3D Slicer Training Documentation https://www.slicer.org/wiki/Documentation/4.10/Training
