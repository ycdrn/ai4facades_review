# A Review on AI Applications for Facades

[Ayca Duran](https://systems.arch.ethz.ch/ayca-duran), [Christoph Waibel](https://systems.arch.ethz.ch/christoph-waibel), [Valeria Piccioni](https://systems.arch.ethz.ch/valeria-piccioni), [Bernd Bickel](https://berndbickel.com/about-me), [Arno Schlueter](https://systems.arch.ethz.ch/arno-schlueter)

[[ Paper ]](https://www.sciencedirect.com/science/article/pii/S0360132324011521) – Published in Building and Environment, February 2025

## Table of Contents
1. [Abstract](#abstract)
2. [Model Setup Instructions](#model-setup-instructions)
3. [Citation](#citation)
4. [Acknowledgements](#acknowledgements)

## Abstract
This review applies a transformer-based topic model to reveal trends and relationships in Artificial Intelligence (AI)-driven facade research, with a focus on architectural, environmental, and structural aspects. AI methods reviewed include Machine Learning (ML), Deep Learning (DL), and Computer Vision (CV). Overall, a significantly growing interest in applying AI methods can be observed across all research areas. However, noticeable differences exist between the three topics. While CV and DL techniques are applied to image data in research on the architectural design of facades, research on environmental aspects of facades often uses numerical data with relatively small datasets and classical ML models. Research on facade structure also tends to use image data but also incorporates numerical performance prediction. A major limitation remains a lack of generalizability, which could be addressed by more comprehensive datasets and novel DL techniques. These include concepts such as Physics-Informed Neural Networks, where domain knowledge is integrated into hybrid data-driven models, and multi-modal diffusion models, which offer generative modeling capabilities to support inverse and forward design tasks. The trends and directions outlined in this review suggest that AI will continue to advance facade research and, in line with other domains, has the potential to achieve a level of maturity suitable for adoption beyond academia and into practice.

![Schematic representation of overall method.](/method.png)

## Model Setup Instructions
This repository contains the dataset, the pre-trained topic model, and a Python notebook to demonstrate the use of the pre-trained model. 

### Prerequisites
- Anaconda or Miniconda must be installed on your machine. You can download it from [Anaconda's site](https://www.anaconda.com/products/individual).

### Environment Setup
The specific versions of Python and all dependencies used are critical for ensuring the model functions correctly. These versions are documented in:
- `python_version.txt`: Contains the Python version used.
- `environment.yml`: Contains all dependencies installed via conda and pip.

To ensure full compatibility and reproducibility, follow these steps to recreate the Python environment used for this model:

1. **Create the environment using the provided YAML file**:
   - Open your terminal.
   - Navigate to the directory containing `environment.yml`.
   - Create the conda environment by running:
     ```bash
     conda env create -f environment.yml
     ```

2. **Activate the new environment**:
   - Once the environment is created, activate it using:
     ```bash
     conda activate [your-env-name]
     ```
   - Replace `[your-env-name]` with the name specified at the top of the `environment.yml` file.

### Model Loading
After setting up the environment, you can load the model using the following steps:

- Navigate to the directory containing the model files.
- Load the model in your Python script or Jupyter Notebook:
  ```python
  from bertopic import BERTopic
  topic_model = BERTopic.load("path/to/my/model_dir")

Alternatively, take a look at the Python notebook for demonstration.

## Citation
If using our dataset/model, please cite us as follows:
```bibtex
@article{DURAN2025112310,
title = {A review on artificial intelligence applications for facades},
journal = {Building and Environment},
volume = {269},
pages = {112310},
year = {2025},
issn = {0360-1323},
doi = {https://doi.org/10.1016/j.buildenv.2024.112310},
author = {Ayca Duran and Christoph Waibel and Valeria Piccioni and Bernd Bickel and Arno Schlueter},
}
```

## Acknowledgements

- [BERTopic](https://maartengr.github.io/BERTopic/index.html)
    
This research was conducted at the Future Cities Lab Global at ETH Zurich. Future Cities Lab Global is supported and funded by the National Research Foundation, Prime Minister’s Office, Singapore under its Campus for Research Excellence and Technological Enterprise (CREATE) programme and ETH Zurich (ETHZ), with additional contributions from the National University of Singapore (NUS), Nanyang Technological University (NTU), Singapore and the Singapore University of Technology and Design (SUTD). This study is supported by the A/T doctoral fellowship offered by the Institute of Technology in Architecture at ETH Zurich.
