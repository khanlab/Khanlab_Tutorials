# Khanlab Tutorial 4: Data visualization

| | |
|-|-|
| date: | Oct 9, 2019 |
| slides: |   |
| screen cast: | [play](https://youtu.be/zTeg9E3stkk) |

## Objective:
Learn about a number of visualization tools and how to use them including FSLeyes, ITKSnap, 3DSlicer, and Paraview!

## Prerequisites (Homework! Do this on your own before the tutorial):
* BRING A MOUSE if you have one handy! It will make navigating the data much easier.
* To be able to follow along with the full tutorial please download and install the latest versions of:
    * [FSLeyes](https://users.fmrib.ox.ac.uk/~paulmc/fsleyes/userdoc/latest/install.html)
    * [ITK-SNAP](http://www.itksnap.org/pmwiki/pmwiki.php?n=Downloads.SNAP3)
    * [3D Slicer](https://download.slicer.org/)
    * [Paraview](https://www.paraview.org/)
    * _Note: You can use these tools via tigerVNC. but it does not allow for full functionality (e.g., Melodic on FSLeyes)._
* Download the data!
    * See the [data section](#data)

## At the end of this tutorial, you will know how to:

### FSL-Eyes
* Load structural images and overlays
* Optimize the view window (min/max intensity, greyscale/other)
* Run FSL MELODIC ICA and load in FSLeyes to view noise/real components

### ITK-SNAP
* Load structural images and 3D segmentations (e.g., from Freesurfer)
* Create NEW 3D segmentations using tools like free draw, active contour
* View and navigate segmentations in the 3D window


### 3D Slicer
* Load structural images and 3D segmentations
* Create 3D segmentations with segment editor
* Use interactive Landmark Registration module


### Paraview
* Visualize neuroimaging models & data on Paraview.
* Create multiple renderers to view / compare data
* Shortcuts & filters for manipulating loaded data
* View / create animations via paraview (great for visualizing tractography)



## Tasks:

### FSL-Eyes
* Load T1 image, load overlay segmentation
* Run melodic ICA code.
* Save folder = melodic.ica
* load folder melodic.ica in melodic view
* view some noise and real components and make .txt to use for the filtering command

### ITK-SNAP
* Load T1 iamge, Load segmentation (Hippocampal?), view on 3 windows + 3D window
* Create new segmentation: hippocampal. Dark band label, slice by slice (save segmentation), grow segmentation (save segmentation), load seg1 (darkband).


### 3D Slicer
* Load T1w image, load segmentation (temporal lobe neocortex)
* Demo segmentation module
* Demo landmark registration module to register ex-vivo image and histology slides

### Paraview
* Check on prerequisite (installation)
* Demo paraview
* Multiple render windows
* Animations

## Data: <a name=data></a>

Data for this tutorial is available on Graham (Compute Canada). If you have access to Graham, you can copy this data to your scratch folder using the following command.

`cp /scratch/tkai/Khanlab_Tutorial5 /scratch/$USER`

If you do not have access to Graham, the data is available for download on [OSF](https://osf.io/4w6ch/).

## Notes:
* Paraview can also perform other analyis (eg. finite-element modelling)

## Resources:
* Sharcnet Webinar on Paraview (2017): https://www.youtube.com/watch?v=yexB3W2FYM0
    * Good resource for learning about the extensive capabilities of paraview
* 3D Slicer Training Documentation https://www.slicer.org/wiki/Documentation/4.10/Training
