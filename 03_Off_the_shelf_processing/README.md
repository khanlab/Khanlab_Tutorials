# Khanlab Tutorial 3: Off the shelf processing

| | |
|-|-|
| date: | Oct 4, 2019 |
| slides: |   |
| screen cast: |  |

## Objective:
 * Demonstrate how containers (Singularity) can be used to run pre-packaged apps and environments on Compute Canada, and how to use neuroglia-helpers to easily run BIDS Apps across nodes. 
 
## Prerequisites (Homework! Do this on your own before the tutorial):
 * To follow along, need to have either compute canada access or access to a Linux machine with singularity installed (preferably latest version 3.4)
 * If containers or singularity is new to you, go through slides/videos listed in resources below
 * If BIDS Apps are new to you, go through paper and website listed in BIDS Apps resources below
 * Review how jobs are created and submitted on SLURM/Compute Canada: https://docs.computecanada.ca/wiki/Running_jobs
 
## At the end of this tutorial, you will know:
 * How to run singularity containers on compute canada
 * How to set-up neuroglia-helpers
 * How to use bidsBatch to batch run configured BIDS apps 
 * How to add new apps or versions to bidsBatch via a github pull request
 * What are some other easy ways to submit jobs with neuroglia-helpers
 
## Tasks:
 * What is singularity
   * singularity run
   * singularity shell
   * singularity exec
   * binding paths
    * watch out for ~/.local 
 * Using singularity on compute canada from scratch (without neuroglia-helpers)
   * BIDS Apps basic usage
   * Creating a job to run mriqc
 * Setting up neuroglia-helpers
 * Running a bidsBatch job (e.g. mriqc)
   * required arguments
   * feeding options to bidsBatch, and options to the BIDS app itself
   * job-templates and default options
 * Adding new apps/versions with a pull request
 * Walkthrough of other scripts in neuroglia-helpers
   * shortcuts for tar2bids, cfmm2tar, dicom2tar, validator, listNumberFiles
   * neuroglia, neurogliaSubmit, regularSubmit, and SINGULARITY_IMG env var
   * neurogliaBatch, regularBatch
   * joblistSubmit, joblistSubmitSequential
   * regularInteractive
 
## Data:

## Notes:

## Resources:

 ### Singularity and Containers background info:
   * Slides from an introduction to singularity: https://www.sdsc.edu/assets/docs/events/introduction-to-singularity.pdf
   * Short (20-min) presentation on singularity: https://youtu.be/29NLgM9fnh4
   * Longer (1hr) presentation on singularity: https://youtu.be/DA87Ba2dpNM
 ### BIDS Apps background info:
   * http://bids-apps.neuroimaging.io/apps/
   * Paper describing BIDS Apps: https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005209

