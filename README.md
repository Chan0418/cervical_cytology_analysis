# cervical_cytology_analysis

# An Analysis on Cervical Cancer Risks and Early Detection 

This project develops a deep learning framework for cervical cytology image classification and pre-cancerous cell localisation using the RIVA dataset. The project compares several classification models, evaluates multi-class classification settings, and uses localisation models to highlight suspected pre-cancerous cell regions.

The final system combines image-level classification with localisation outputs to support visual interpretation. This project is for academic research and portfolio purposes only, and is not intended for clinical diagnosis or medical decision-making.

## Project Overview

Cervical cancer screening is important for early detection, but manual Pap smear examination can be time-consuming and affected by observer differences. This project explores deep learning methods that can classify cervical cytology images and provide visual localisation outputs for suspected abnormal cell regions.

The project includes:

- Exploratory data analysis of the RIVA dataset
- Binary classification of pre-cancerous and non-lesion images
- Multi-class classification using six-class, seven-class and eight-class settings
- Localisation using U-Net and Stacked Hourglass models
- Integrated prediction pipeline using the best binary classifier as a gate for localisation outputs
- Result visualisation using tables, plots, heatmaps and prediction examples

## Dataset

This project uses the RIVA dataset:

**RIVA: An Image Dataset of Conventional Pap Smear Cytology with Multiple Independent Annotations**  
Dataset DOI: `10.5281/zenodo.17288879`  
Dataset source: Zenodo

RIVA is a conventional Pap smear cytology dataset developed for research in automated cervical cancer screening and diagnostic decision support. It contains 959 mini-patches extracted from real cytological samples, including 386 mini-patches annotated independently by four expert cytologists and 573 mini-patches annotated by a single expert.

The dataset includes 26158 expert annotations, with labels covering SCC, HSIL, ASC-H, LSIL, ASC-US, INF, ENDO and NILM.

Due to dataset size and licensing considerations, the dataset is not included in this repository. Users should download the dataset manually from Zenodo and place it locally using the following structure:

```text
data/
└── riva_1.0/
    ├── images/
    └── annotations/
        └── annotations.json
