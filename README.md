# Structure and Ligand-Based Discovery of Novel 3CLpro Non-peptidomimetic Hits

## 📋 Overview

This repository contains the code and data for the discovery of novel non-peptidomimetic compounds with activity against the SARS-CoV-2 main protease (3CLpro), utilizing structure-based and ligand-based approaches.

The project implements three complementary approaches:
- **Machine Learning Models** - Training and validation of predictive models using curated datasets
- **Ensemble Docking** - Structure-based virtual screening using multiple protein conformations
- **Shape-Based Screening** - Ligand-based virtual screening using molecular shape similarity

## 📁 Repository Structure

```
├── MLmodel/
│   ├── Code/
│   │   ├── Colab_train.ipynb    # Training notebook (Google Colab)
│   │   └── Colab_VS.ipynb        # Virtual screening notebook (Google Colab)
│   ├── Data/
│   │   └── Curated_data.sdf      # Curated compound dataset
│   └── Model/                     # Trained ML models (RF, SVM, LightGBM)
│
├── ensemble_docking/
│   ├── data/                      # Active, inactive, and decoy compounds
│   ├── Grids/                     # Docking grid files
│   └── validation/                # Validation results
│
├── Shapemodel/
│   ├── data/                      # Actives and inactives for shape screening
│   ├── compound21-query.sq        # Shape query file
│   └── validation/                # Validation results
│
└── README.md
```

## 🚀 Methodologies

### Machine Learning Models

The Jupyter notebooks were developed and executed on **Google Colab**, leveraging cloud-based computational resources:

- `MLmodel/Code/Colab_train.ipynb` - Training and validation of ML models using multiple fingerprints (Morgan, MACCS, FeatMorgan) and algorithms (Random Forest, SVM, LightGBM)
- `MLmodel/Code/Colab_VS.ipynb` - Virtual screening implementation for hit identification

### Ensemble Docking

Structure-based virtual screening performed using multiple 3CLpro conformations to account for protein flexibility. Contains validated active compounds, inactives, and decoy sets for benchmarking.

### Shape-Based Screening

Ligand-based approach using molecular shape similarity to identify compounds with structural features similar to known 3CLpro inhibitors.

## 🔬 Data

- **MLmodel/Data/Curated_data.sdf** - Curated dataset containing chemical structures and biological activity information against SARS-CoV-2 3CLpro
- **ensemble_docking/data/** - Active compounds (≤10 μM), decoys, and inactive compounds for docking validation
- **Shapemodel/data/** - Active and inactive compound sets in OpenEye format for shape-based screening

## 💻 Usage

### Machine Learning Workflow
1. Open the notebooks in Google Colab by uploading the `.ipynb` files from `MLmodel/Code/`
2. Upload the necessary data from the `MLmodel/Data/` folder
3. Execute the cells sequentially following the instructions in each notebook
4. Trained models will be saved in `MLmodel/Model/`

### Ensemble Docking
Navigate to the `ensemble_docking/` directory and follow the docking protocol using the provided grids and validation datasets.

### Shape-Based Screening
Use the shape query file in `Shapemodel/` with the provided active/inactive datasets for ligand-based virtual screening.

## 🎯 Objective

To identify and prioritize promising non-peptidomimetic compounds as potential inhibitors of 3CLpro, a key target protein for the development of antivirals against SARS-CoV-2, through the integration of complementary computational approaches.

## 📄 License

This project is licensed under the terms specified in the LICENSE file.