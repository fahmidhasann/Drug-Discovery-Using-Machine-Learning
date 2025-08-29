# Drug Discovery Using Machine Learning

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A QSAR (Quantitative Structure-Activity Relationship) model for predicting acetylcholinesterase inhibition using machine learning and cheminformatics. This project demonstrates computational drug discovery techniques for identifying potential Alzheimer's disease treatments.

## Overview

Acetylcholinesterase (AChE) is a key enzyme targeted in Alzheimer's disease therapy. This project builds predictive models to identify potential AChE inhibitors from chemical structures using bioactivity data from the ChEMBL database.

**Dataset**: ~6,000 compounds from ChEMBL (Target: CHEMBL220)  
**Features**: Molecular descriptors and PubChem fingerprints  
**Target**: IC50 values for AChE inhibition  

## Quick Start

### 1. Clone Repository
```bash
git clone https://github.com/fahmidhasann/Drug-Discovery-Using-Machine-Learning.git
```

### 2. Navigate to Directory
```bash
cd Drug-Discovery-Using-Machine-Learning
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook "Drug Discovery Using Machine Learning.ipynb"
```

## Methodology

1. **Data Collection**: Retrieve bioactivity data from ChEMBL database
2. **Preprocessing**: Clean data, handle missing values, convert IC50 to pIC50
3. **Feature Engineering**: Calculate Lipinski descriptors and molecular fingerprints
4. **Modeling**: Train Random Forest regressor and compare multiple algorithms
5. **Evaluation**: Statistical analysis and model performance assessment

## Key Results

- **Primary Model**: Random Forest Regressor (500 estimators)
- **Feature Selection**: Variance threshold filtering applied
- **Significant Descriptors**: Molecular Weight, LogP, Hydrogen Bond Donors
- **Statistical Testing**: Mann-Whitney U tests for bioactivity class differences

## Repository Structure

```
├── Drug Discovery Using Machine Learning.ipynb  # Main analysis
├── df_final.csv                                # Processed data
├── fingerprint.csv                             # Molecular fingerprints
├── smiles_id.smi                              # Chemical structures
├── requirements.txt                            # Dependencies
└── README.md                                   # Documentation
```

## Requirements

- Python 3.7+
- Key libraries: pandas, numpy, scikit-learn, rdkit, chembl-webresource-client
- See `requirements.txt` for complete list

## Author

**Fahmid Hasan Taohid**  
B.Sc. in Agriculture (Hons), Bangladesh Agricultural University  
Email: taohid.2102010@bau.edu.bd

## Acknowledgments

- [ChEMBL Database](https://www.ebi.ac.uk/chembl/) for bioactivity data
- [Data Professor](https://www.youtube.com/@DataProfessor) for educational content
- RDKit and scikit-learn communities

## License

MIT License - see [LICENSE](LICENSE) file for details.