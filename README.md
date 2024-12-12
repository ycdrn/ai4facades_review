# A Review on AI Applications for Facades

[Ayca Duran](https://systems.arch.ethz.ch/ayca-duran), [Christoph Waibel](https://systems.arch.ethz.ch/christoph-waibel), [Valeria Piccioni](https://systems.arch.ethz.ch/valeria-piccioni), [Bernd Bickel](https://berndbickel.com/about-me), [Arno Schlueter](https://systems.arch.ethz.ch/arno-schlueter)

[[ Paper ]](https://www.sciencedirect.com/science/article/pii/S0360132324011521) – Published in Building and Environment, February 2025

## Description
This repository contains the dataset, the pre-trained topic model, and a Python notebook to demonstrate the use of the pre-trained model. 

## Model Setup Instructions

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
