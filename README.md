# Building Footprint Extraction from High-Resolution Aerial Imagery Using Deep Learning

## Overview

This repository documents a practical implementation of deep learning approaches for building detection and footprint extraction from high-resolution aerial imagery.

The project explores the application of computer vision techniques to remote sensing data, with a focus on identifying building structures and extracting their spatial footprints.

The implementation uses NAIP aerial imagery and Overture Maps building data as a geospatial reference, exploring two deep learning approaches:

- **U-Net:** Semantic segmentation.

## Study Area and Data

- **Study area:** Knoxville, Tennessee, USA.
- **Imagery source:** National Agriculture Imagery Program (NAIP).
- **Spatial resolution:** 0.6 metres.
- **Building reference data:** Overture Maps.
- **Dataset scale:** Up to approximately 200 buildings.

## Methodology

The workflow involved:

1. Acquiring and preparing high-resolution aerial imagery.
2. Obtaining building reference information from Overture Maps.
3. Preparing imagery and corresponding building labels.
4. Implementing Faster R-CNN for building object detection.
5. Implementing U-Net for semantic segmentation.
6. Evaluating model performance using standard segmentation metrics.
7. Generating and visualizing building extraction results.

## Model Evaluation

The U-Net model achieved the following validation results at epoch 15:

| Evaluation metric | Score |
|---|---:|
| Intersection over Union (IoU) | 0.9032 |
| F1-score | 0.9479 |
| Precision | 0.9488 |
| Recall | 0.9472 |

These values represent results from the validation setup and should not be interpreted as independent performance benchmarks across other geographical areas.

## Results

The project produced building segmentation outputs and spatial visualizations illustrating the distribution and extraction of building features within the study area.

See the `results/` directory for available evaluation and visualization outputs.

## Relevance and Potential Applications

Building footprint extraction from aerial imagery has applications in:

- Urban mapping and building inventory development.
- Geospatial asset mapping.
- Land-use and urban growth analysis.
- Property intelligence and spatial analytics.
- As a foundation for further research into multi-temporal building change detection.

## Limitations

This implementation was based on a relatively small dataset. 

Further work would require independently prepared datasets, additional validation, and testing across different geographical environments.

## Future Work

Potential extensions include:

- Testing on imagery from different geographical environments.
- Building a larger and independently annotated training dataset.
- Evaluating model generalization.
- Investigating multi-temporal building change detection.
- Exploring construction-stage classification using imagery and ground-level observations.

## Acknowledgements

Wu, Q. (2026). GeoAI with Python: A Practical Guide to Open-Source Geospatial AI. Independently published. PDF edition ISBN 979-8993859729; Print edition ISBN 979-8253507414
