# ImplicitTerrain: Continuous Surface Modeling for Terrain Data Analysis

## Introduction
ImplicitTerrain leverages Implicit Neural Representations (INR) to model high-resolution terrain continuously and differentiably, enhancing the accuracy of surface representation and topological information restoration. This project offers a novel pipeline, making use of the Surface-plus-Geometry (SPG) cascaded INR model for terrain surface modeling, maintaining high reconstruction fidelity and enabling direct topological analysis on the continuous manifold.

## Key Features
- **High Fidelity Surface Modeling:** Utilizes a novel SPG model for precise terrain representation.
- **Progressive Training Strategy:** Improves convergence speed and efficiency during model training from coarse to fine scales.
- **Topological and Topographical Analysis:** Integrates extracted topological features with discrete Morse theory and supports calculations of various topographical features directly from surface derivatives.

## Implementation Details
Our codebase is ongoing a refactorization for further developement. For ImplicitTerrain, the neural network structure and fitting is straightforward:
* The implementation of ImplicitTerrain is based on the PyTorch implementation of the [SIREN](https://github.com/vsitzmann/siren). Model configuration and training settings are detailed in the Experiment section of the paper.
* Surface model's gradient calculation is based on the PyTorch autograd mechanism.
* Image downsampling and smoothing are implementation by [Skimage](https://scikit-image.org/) and image gradient calculation is implemented by [Numpy](https://numpy.org/).
* *Forman method* results are based on an open-source library [FormanGradient2D](https://github.com/UMDGeoVis/FormanGradient2D).


## Acknowledgments
This work was supported by the US National Science Foundation under grant number IIS-1910766.
