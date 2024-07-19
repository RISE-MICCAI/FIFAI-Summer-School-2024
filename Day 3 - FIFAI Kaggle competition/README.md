# 📘 FIFAI Kaggle Notebook

## Overview

Welcome to the **FIFAI Kaggle competition**! This notebook is designed to help you get started with the competition. It includes everything you need to load the data, set up the environment, train models, and make submissions.

## Contents

- **Data Loading**: Instructions to load and preprocess the dataset.
- **Model Training**: Simple models to get you started and examples of more complex models.
- **Evaluation Metrics**: Tools to evaluate the performance of your models.
- **Submission**: Code to generate and submit predictions to Kaggle.

## Getting Started

### Prerequisites

The notebook was designed to be used online on Google Colab, but should you prefer running it locally, you can use conda to create the environment from the `environment.yml` file provided or create a new environment and install the dependencies using the `requirements.txt` file. If you are not familiar with conda, take a look at setting up conda [here](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html).

If you are not familiar with Jupyter notebooks, you can get started [here](https://jupyter.org/install).

### Use Environment

To create and activate the Conda environment from the `environment.yml` file:

```sh
conda env create -f environment.yml
conda activate FIFAI_Kaggle
python -m ipykernel install --user --name=FIFAI_Kaggle --display-name "FIFAI_Kaggle"
```

### Use requirements
You can install the required dependencies yourself from the 'requirements.txt' file as well

```sh
conda create --name FIFAI_Kaggle --file requirements.txt
conda activate FIFAI_Kaggle
python -m ipykernel install --user --name=FIFAI_Kaggle --display-name "FIFAI_Kaggle"
```

## Data
Ensure you have downloaded all the necessary files from the Kaggle competition page. Place the data files in the appropriate directory as specified in the notebook.

# Usage
Open the Notebook: Upload notebook, FIFAI_Kaggle_Competition.ipynb, to Google colab or Launch Jupyter Notebook locally and open the notebook.
Run the Cells: Execute the cells in the notebook sequentially. Make sure to read the instructions and comments provided in each cell.
Customize and Experiment: Feel free to modify the code, experiment with different models, and improve upon the baseline.
Teamwork
Remember to work collaboratively with your team. Each team should designate a representative for submitting the predictions on Kaggle.

# Troubleshooting
If you encounter any issues or have any questions, please reach out to the competition organizers or consult the Kaggle discussion forum.

# License
This project is licensed under the MIT License - see the LICENSE file for details.

# Acknowledgments
Kaggle for hosting the competition.
MedMNIST for providing the dataset.
FIFAI Summer School team.
All the contributors and participants for their efforts and collaboration.

# Author
This notebook and the contents associated with it were created by Michael Alummoottil.