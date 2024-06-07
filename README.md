# DILI - Drug-Induced Liver Injury Prediction

## Overview
DILI is a comprehensive repository aimed at enhancing the early detection of Drug-Induced Liver Injury (DILI) through the integration of predicted in vivo and in vitro data. This project utilizes advanced machine learning models and chemical informatics to predict the likelihood of DILI for various compounds.

## Features
- Integration of in vivo and in vitro data for improved DILI prediction.
- Utilizes pharmacokinetic parameters, structural fingerprints, and physicochemical parameters.
- Eleven proxy-DILI labels from datasets such as mitochondrial toxicity, bile salt export pump inhibition, and preclinical rat hepatotoxicity studies.
- Available as both a command-line interface (CLI) and a Python library.

## Installation

### Using PyPI
You can install the DILI Predictor using pip: `pip install dilipred`

### Building from Source
You can also build from source using python-poetry:
1. Clone the repository: `git clone https://github.com/Manas02/dili-pip.git`
2. Navigate to the project directory: `cd dili-pip/`
3. Install dependencies: `poetry install`
4. Activate the virtual environment: `poetry shell`
5. Build the project: `poetry build`

## Usage

### Running DILIPredictor as CLI
To get started with the CLI, use: `dili -h`

### Predicting DILI for a Single Molecule
Select from the sidebar to predict DILI for a single molecule.

### Running DILIPredictor as Library
Here's a basic example of how to use DILIPredictor as a Python library:

```python
from dilipred import DILIPRedictor

if __name__ == '__main__':
    dp = DILIPRedictor()
    smiles = "CCCCCCCO"
    result = dp.predict(smiles)
    print(result)
```

# Repository Structure
- `data/` : Contains datasets used in the project.
- `00_Create_livtox_dili_datasets.ipynb` : Notebook to create DILI datasets.
- `01_Split_Train_Test_Datasets.ipynb` : Notebook to split datasets into training and testing sets.
- `02_Explore_Chemical_Spaces_PCA_TSNE-.ipynb` : Notebook to explore chemical spaces using PCA and t-SNE.
- `03a_Create_Cmax_models.ipynb` : Notebook to create Cmax models.
- `03b_predCmax_DILI_Scores.ipynb` : Notebook to predict Cmax DILI scores.
- `03c_Create_combination_models_v2.ipynb` : Notebook to create combination models.
- `04_Compare_Performance_NCV.ipynb` : Notebook to compare model performance using nested cross-validation.
- `05a_Find_AUC_Regions_v2.ipynb` : Notebook to find AUC regions.
- `05c_Compare_FPR.ipynb` : Notebook to compare false positive rates.
- `08_check_chemistry_12trainingcompounds.ipynb` : Notebook to check chemistry of 12 training compounds.
- `08_check_chemistry_4compounds.ipynb` : Notebook to check chemistry of 4 compounds.
- `Cmax_processed.csv` : Processed Cmax data.
- `Heldout_test_predictions_earlydetection.csv` : Predictions for held-out test data for early detection.
- `Test_data_DILIst.csv` : Test data for DILI.
- `all_features_desc.csv` : Description of all features.
- `mordred_desc.csv` : Description of Mordred features.
- `test_data_heldouttest_DILIst_223.csv` : Held-out test data for DILI.
- `test_data_ncv_DILIst_888.csv` : Nested cross-validation test data for DILI.

## Citation
If you use DILI Predictor in your work, please cite:

Improved Early Detection of Drug-Induced Liver Injury by Integrating Predicted in vivo and in vitro Data; Srijit Seal, Dominic P. Williams, Layla Hosseini-Gerami, Ola Spjuth, Andreas Bender bioRxiv 2024.01.10.575128; doi: https://doi.org/10.1101/2024.01.10.575128

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgements
Developed and maintained by Srijit Seal and contributors.

## Contact
For any questions or issues, please open an issue on the GitHub repository.
