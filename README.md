# FACADE-AI Literature Review

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
