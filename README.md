# Structure and Ligand-Based Discovery of Novel 3CLpro Non-peptidomimetic Hits

## 📋 Overview

This repository contains the code and data for the discovery of novel non-peptidomimetic compounds with activity against the SARS-CoV-2 main protease (3CLpro), utilizing structure-based and ligand-based approaches.

The project implements machine learning workflows for:
- **Training predictive models** using curated datasets of active and inactive compounds
- **Virtual screening** of compound libraries to identify potential hits

## 🚀 Notebooks

The Jupyter notebooks were developed and executed on **Google Colab**, leveraging cloud-based computational resources:

- `Code/Colab_train.ipynb` - Training and validation of machine learning models
- `Code/Colab_VS.ipynb` - Virtual screening implementation for hit identification

## 📁 Repository Structure

```
├── Code/
│   ├── Colab_train.ipynb    # Training notebook (Google Colab)
│   └── Colab_VS.ipynb        # Virtual screening notebook (Google Colab)
├── Data/
│   └── Curated_data.sdf      # Curated compound dataset
├── Model/                     # Trained models
└── README.md
```

## 🔬 Data

The curated dataset (`Curated_data.sdf`) contains chemical structures and biological activity information against SARS-CoV-2 3CLpro.

## 💻 Usage

1. Open the notebooks in Google Colab by clicking on the links or uploading the `.ipynb` files
2. Ensure the necessary data from the `Data/` folder is uploaded
3. Execute the cells sequentially following the instructions in each notebook

## 🎯 Objective

To identify and prioritize promising non-peptidomimetic compounds as potential inhibitors of 3CLpro, a key target protein for the development of antivirals against SARS-CoV-2.

## 📄 License

This project is licensed under the terms specified in the LICENSE file.