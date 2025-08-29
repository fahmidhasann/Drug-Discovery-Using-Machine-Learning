# Drug Discovery Using Machine Learning: QSAR Model for Acetylcholinesterase Inhibition

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![ChEMBL](https://img.shields.io/badge/ChEMBL-Database-green)](https://www.ebi.ac.uk/chembl/)
[![RDKit](https://img.shields.io/badge/RDKit-Cheminformatics-red)](https://www.rdkit.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🔬 Project Overview

This project demonstrates the application of **machine learning** and **cheminformatics** in drug discovery by building a **QSAR (Quantitative Structure-Activity Relationship)** model to predict the inhibitory activity of chemical compounds against **Acetylcholinesterase (AChE)**. The model serves as a powerful tool for identifying potential drug candidates for Alzheimer's disease treatment and understanding pesticide mechanisms.

### 🎯 Key Objectives
- Build predictive models for acetylcholinesterase inhibition
- Analyze chemical structure-activity relationships
- Compare multiple machine learning algorithms for drug discovery
- Generate molecular fingerprints for computational analysis
- Provide insights into chemical properties affecting bioactivity

## 🧬 About Acetylcholinesterase (AChE)

**Acetylcholinesterase** is a crucial enzyme that breaks down acetylcholine into choline and acetate, playing a vital role in nerve signal transmission. Understanding AChE inhibition is important for:

### 🧠 **Alzheimer's Disease Treatment**
- AChE inhibitors increase acetylcholine levels in the brain
- Helps improve memory and cognitive function
- Current FDA-approved drugs target this enzyme

### 🐛 **Pesticide Development**
- Many pesticides work by inhibiting AChE in insects
- Disrupts nervous system function in target pests
- Important for agricultural applications

### ⚕️ **Toxicology Research**
- Understanding AChE helps develop treatments for chemical poisoning
- Critical for safety assessment of new compounds

## 🛠️ Technical Implementation

### 📊 **Data Pipeline**
1. **Data Retrieval**: Bioactivity data from ChEMBL database
2. **Data Preprocessing**: Cleaning, filtering, and standardization
3. **Feature Engineering**: Molecular descriptor calculation
4. **Model Training**: Multiple ML algorithms comparison
5. **Evaluation**: Performance metrics and visualization

### 🔍 **Dataset Characteristics**
- **Source**: ChEMBL Database (Target: CHEMBL220)
- **Compounds**: ~6,000 chemical structures
- **Activity Measure**: IC50 values (converted to pIC50)
- **Classification**: Active (IC50 ≤ 1,000 nM), Inactive (IC50 ≥ 10,000 nM)

### 🧪 **Molecular Descriptors**
- **Lipinski's Rule of Five**: MW, LogP, HBD, HBA
- **PubChem Fingerprints**: 881-bit molecular fingerprints
- **Statistical Analysis**: Mann-Whitney U tests for significance

## 📁 Repository Structure

```
Drug-Discovery-Using-Machine-Learning/
├── Drug Discovery Using Machine Learning.ipynb  # Main analysis notebook
├── df_final.csv                                # Processed bioactivity data
├── fingerprint.csv                             # Molecular fingerprints
├── smiles_id.smi                              # SMILES chemical structures
├── fingerprints_xml.zip                       # PaDEL descriptor configurations
└── README.md                                   # Project documentation
```

## 🚀 Getting Started

### Prerequisites
```bash
python>=3.7
jupyter
pandas
numpy
scipy
rdkit
scikit-learn
seaborn
matplotlib
chembl_webresource_client
padelpy
lazypredict
```

### Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/fahmidhasann/Drug-Discovery-Using-Machine-Learning.git
   cd Drug-Discovery-Using-Machine-Learning
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or install individually:
   ```bash
   pip install chembl_webresource_client pandas numpy scipy rdkit padelpy scikit-learn lazypredict seaborn matplotlib
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook "Drug Discovery Using Machine Learning.ipynb"
   ```

## 📈 Key Results

### 🎯 **Model Performance**
- **Random Forest Regressor**: Primary model with 500 estimators
- **R² Score**: High correlation between predicted and experimental values
- **Feature Selection**: Variance threshold filtering applied

### 📊 **Statistical Insights**
- **Significant Descriptors**: Molecular Weight, LogP, Hydrogen Bond Donors
- **Non-significant**: Hydrogen Bond Acceptors (p > 0.05)
- **Data Distribution**: Log-normal transformation improved model performance

### 🔬 **Chemical Space Analysis**
- Active and inactive compounds occupy similar chemical descriptor space
- Clear separation in pIC50 values as expected
- Molecular fingerprints provide detailed structural information

## 🔧 Methodology

### 1. **Data Collection & Preprocessing**
- Query ChEMBL database for AChE bioactivity data
- Filter for IC50 measurements and human targets
- Remove missing values and invalid SMILES

### 2. **Feature Engineering**
- Calculate Lipinski descriptors using RDKit
- Generate PubChem fingerprints via PaDEL-Descriptor
- Apply variance threshold for feature selection

### 3. **Exploratory Data Analysis**
- Statistical hypothesis testing (Mann-Whitney U)
- Visualization of chemical space
- Bioactivity class distribution analysis

### 4. **Model Building**
- Train-test split (80:20 ratio)
- Random Forest regression as primary model
- Comprehensive algorithm comparison using LazyPredict

### 5. **Model Evaluation**
- R-squared correlation analysis
- Scatter plot visualization
- Cross-validation performance metrics

## 📚 Learning Resources

This project was inspired by the excellent tutorial from **Data Professor** YouTube channel:
- 🎥 [Data Professor Channel](https://www.youtube.com/@DataProfessor)
- 📖 Comprehensive cheminformatics and machine learning tutorials
- 🔬 Practical applications in drug discovery

## 👨‍🔬 About the Author

**Fahmid Hasan Taohid**
- 🎓 B.Sc. in Agriculture (Hons), Bangladesh Agricultural University
- 🔬 Passionate about computational agriculture and data science
- 💡 Exploring the intersection of technology and agricultural research

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **ChEMBL Database** for providing high-quality bioactivity data
- **RDKit** for cheminformatics toolkit
- **Data Professor** for educational content and inspiration
- **Open source community** for amazing tools and libraries

## 📞 Contact

- **GitHub**: [@fahmidhasann](https://github.com/fahmidhasann)
- **Email**: [Contact via GitHub](https://github.com/fahmidhasann)

---

⭐ **If you find this project helpful, please consider giving it a star!** ⭐