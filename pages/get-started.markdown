---
layout: page
title: Get Started
permalink: /pages/get-started
---

# Prerequisites 

We recommended cloning the  [CoCoNest GitHub repository](https://github.com/sbci-brain/CoCoNest/), along with the [SBCI Toolkit repository](https://github.com/sbci-brain/SBCI_Toolkit) for visualization scripts. The scripts in these repositories are written in MATLAB. 

# Accessing CoCoNest Members 

Various members of the CoConest family can be downloaded from the `members` folder of the [CoCoNest GitHub repository](https://github.com/sbci-brain/CoCoNest/tree/main/members). This folder contains label.gii and .annot files for the parcellations in three popular template spaces: fslr32k, fsaverage, and mni152. 

Label files for other members of the CoCoNest family can be created using the scripts in the `CoCoNest/scripts/GetCoCoMembers/` folder of the CoCoNest Github repository. First, edit the file paths in the config.txt file in `CoCoNest/scripts`. `PARC_NAME` should be set to "CoCoNest", and `OUTPUT_FOLDER` and `FS_SUB_FOLDER` should point to the proper CocoNest and Freesurfer subjects folders. After editting the config.txt file, executing the following command will populate the  `CoCoNest/scripts/output/labels/` folder with the label.gii and .annot files for the requested CoCoNest members in each template space.  

```
getCoCoMembers.sh "5 10 15 25 50 75 100 125 150 175 200 225 250 275 300 325 350 375 400 450 475 500"

```

# Exploring CoCoNest Members 

Recall that the CoCoNest family was created by parcellating 3675 vertices on the brain's surface. Each member of the CoCoNest family corresponds to a subtree of the full CoCoNest tree, and each parcel of a member of the CoCoNest family corresponds to a node in the full tree. The full CoCoNest tree can be accessed through the `link` variable of the pruning structure located at `CoCoNest/scripts/output/TreeResults/CoCoNest_prune_struct.mat`. The link variable is the linkage matrix output by [MATLAB's linkage function](https://www.mathworks.com/help/stats/linkage.html). The linkage matrix contains $$n-1=3675$$ rows and each row represents a single step in the hierarchical clustering process. The first column is the index of the first parcel being merged, the second column is the index of the second parcel being merged, and the third column is the distance between the two parcels being merged. Each of the original $$3675$$ observations are given a parcel index that simply corresponds to its index in the connectivity data, e.g., parcel 1 is the vertex 1. After two parcels are merged, the new parcel is given an index that is sequentially incremented starting from $$n+1 = 3675+1$$. For example, the first row of CoCoNest's linkage matrix is 

```
1628 1630 2.8189
```

This indicates that the first two parcels merged were vertices 1628 and 1630 with a similarity of 2.8189. The new parcel containing vertices 1628 and 1630 is labeled as parcel $$3675 + 1 = 3676$$. 
 


