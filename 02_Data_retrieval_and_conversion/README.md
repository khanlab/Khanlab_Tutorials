# Khanlab Tutorial 2: Data Retrieval and Conversion

| | |
|-|-|
| date: | September 27, 2019 |
| slides: | [download](https://docs.google.com/presentation/d/1zor12oH5fjXIaqTRPtJEt2KDd6MP8e3dgRCGhaWOjXs/edit?usp=sharing) |
| screen cast: | |

## Objective:
Outline the CFMM dicom server operation and how to convert data to BIDS from the dicom server

## Prerequisites (Homework! Do this on your own before the tutorial):

### Accessing data on the CFMM DICOM server
* Please read through the [documentation on accessing data](https://dicom.cfmm.robarts.ca/dm/docs/accessing_data) (To log in, you must have read access to at least one Project's data).
* If you use MacOS and would like to set up the Horos DICOM client to download datasets from the CFMM DICOM Server, please install [Horos](https://horosproject.org/download-horos/) and [DcmProxy](https://gitlab.com/cfmm/dcmproxy/-/jobs/artifacts/0.4/raw/DcmProxy-0.4.dmg?job=build%3Amacos).
* If you want to try out a command-line DICOM search/download tool, please download `dcmtk`:
  * On MacOS, the easiest way is using Homebrew (`brew install dcmtk`).
  * On some Linux distributions, you can install it through your package manager (e.g. `apt install dcmtk` in Ubuntu)
  * ['Chocolatey'](https://chocolatey.org/) is a Windows package manager that also can install `dcmtk`.
  * Otherwise, [compile from source](https://support.dcmtk.org/docs/file_install.html)

### If you don't know what BIDS is go to methods lunch on Sept 23.
Suzanne is presenting a background and we are gonna focus on how to convert data.

## At the end of this tutorial, you will know:

* How to access the CFMM DICOM server and download data from it
* How to download your data as a tarball
* How to get information to set up automated BIDS conversion
* Automated BIDS conversion at cfmm
* How to build a heuristic for a automated BIDS conversion

## Tasks:

* Introduction to DICOMS (Igor)
* CFMM DICOM server organization (Igor)
* non-imaging dicom data (Igor)
* How to download your data on the web (Igor)
* cfmm2tar usage to download tar.gz dicoms (Igor)
* tar2bids command line usage (Olivia)
* heudiconv overview (Olivia)
* heudiconv demo and how to use cfmm_base.py (Olivia)
* heuristics demo  (Olivia)
* autoconversion tips and tricks (Olivia)

## If time allows:

* Horus and dcmproxy demo
* Commandline DICOM tools

## Data:

n/a

## Notes:

## Resources:


