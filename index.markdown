---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page    
---

# CoCoNest - A Continuous Structural Connectivity-based Parcellation

## Introduction 


<img src="imgs/coconest_250.jpg" width="400" height="400">

This webpage is a resource for understanding and using CoCoNest - a fully data-driven, multi-resolution family of parcellations created from structural connectome data. Below you will find a brief introduction to CoCoNest. The "Getting Started" page contains instructions for using the CoCoNest family for exploratory and predictive analyses. The "Planned Updates" page contains a list of upcoming updates to the CoCoNest family and accompanying analysis tools.  


## Why Use CoCoNest? 

The CoCoNest family of parcellations was evaluated using a compresensive collection of internal and external evaluation metrics. These metrics measure a parcellation's alignment with neurobiological intuition and performance in typical downstream tasks. With these metrics, we have shown that members of the CoCoNest family are competitive with widely used parcellations in the neuroscience literature, often showing superior performance across various resolutions (parcellation sizes). Additionally, the CoCoNest family facillitates tractable explorations into the multi-scale nature of the structural connectome, allowing researchers to investigate the interactions and distinctions between multiple resolutions of the structural connectome.  

## How Was CoCoNest Created?

<img src="imgs/parc_pipeline.jpg" width="400" height="400">

To create the CoCoNest family, we leveraged a recently developed tractography algorithm called surface-enhanced tractography (SET) which has been shown to decrease gyral bias and better approximate the underlying white matter structure. Subsequently, we used a continuous representation of structural connectivity, which provides a rigorous statistical framework for modeling white matter fiber track endpoints and constructs dense, high-resolution structural connectivity matrices. Starting with the high-resolution structural connectivity data, we used a conventional agglomerative (bottom-up) clustering algorithm to construct a full binary tree that aims to reflect the hierarchical organization of the structural connectome. We then used error-complexity pruning to iteratively remove branches from this tree in a greedy fashion, balancing the complexity of the tree with its fit to the high-resolution connectome data. This procedure created a nested sequence of subtrees where each subtree corresponded to a member of the CoCoNest family.

The scripts for constructing dense, high-resolution structural connectivity matrices using a continuous framework can be found [here](https://github.com/sbci-brain/SBCI_Pipeline)
Useful tools for visualizing and exploring such connectivity data can be found [here]( https://github.com/sbci-brain/SBCI_Toolkit)


