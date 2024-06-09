---
layout: page
title: Get Started
permalink: /pages/get-started
---

# Prerequisites 

We recommended cloning the CoCoNest Github repository, along with the SBCI Toolkit repository for visualization scripts. The scripts in these repositories are written in MATLAB. 

# Accessing CoCoNest Members 

Various members of the CoConest family can be downloaded from the `members` folder of the [CoCoNest GitHub repository](https://github.com/sbci-brain/CoCoNest/tree/main/members). This folder contains label.gii and .annot files for the parcellations in three popular template spaces: fslr32k, fsaverage, and mni152. 

Label files for other members of the CoCoNest family can be created using the scripts in the `CoCoNest/scripts/GetCoCoMembers/` folder of the CoCoNest Github repository. First, edit the file paths in the config.txt file in `CoCoNest/scripts`. `PARC_NAME` should be set to "CoCoNest", and `OUTPUT_FOLDER` and `FS_SUB_FOLDER` should point to the proper CocoNest and Freesurfer subjects folders. After editting the config.txt file, executing the following command will populate the  `CoCoNest/scripts/output/labels/` folder with the label.gii and .annot files for the requested CoCoNest members in each template space.  

```
getCoCoMembers.sh "5 10 15 25 50 75 100 125 150 175 200 225 250 275 300 325 350 375 400 450 475 500"

```
