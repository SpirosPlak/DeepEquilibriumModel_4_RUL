# A Deep Equilibrium Model for Remaining Useful Life of Aircraft Engines

This repository contains the code implementation for the scientific study titled:  
**"A Deep Equilibrium Model for Remaining Useful Life of Aircraft Engines."**

The work presents a novel approach leveraging **Deep Equilibrium Models (DEMs)** for the prediction of **Remaining Useful Life (RUL)** in aircraft engines. It combines fixed-point modeling with Bayesian calibration to handle uncertainty in degradation forecasting.

## 🧠 Overview

- **Deep Equilibrium Models (DEMs)**: A class of implicit-depth models where the output is a fixed point of a learned dynamical system.
- **Bayesian Inference**: Used for uncertainty quantification in RUL prediction.
- **Dataset**: NASA’s C-MAPSS dataset for turbofan engine degradation simulation.

Estimating Remaining Useful Life (RUL) is crucial in modern Prognostic and
Health Management (PHM) systems providing valuable information for planning the
maintenance strategy of critical components in complex systems such as aircraft engines.
Deep Learning (DL) models have shown great performance in the accurate prediction
of RUL, building hierarchical representations by the stacking of multiple explicit neural
layers. In the current research paper, we follow a different approach presenting a Deep
Equilibrium Model (DEM) that effectively captures the spatial and temporal information
of the sequential sensor. The DEM, which incorporates convolutional layers and a novel
dual-input interconnection mechanism to capture sensor information effectively, estimates
the degradation representation implicitly as the equilibrium solution of an equation, rather
than explicitly computing it through multiple layer passes. The convergence representation
of the DEM is estimated by a fixed-point equation solver while the computation of the
gradients in the backward pass is made using the Implicit Function Theorem (IFT). The
Monte Carlo Dropout (MCD) technique under calibration is the final key component of
the framework that enhances regularization and performance providing a confidence
interval for each prediction, contributing to a more robust and reliable outcome. Simulation
experiments on the widely used NASA Turbofan Jet Engine Data Set show consistent
improvements, with the proposed framework offering a competitive alternative for RUL
prediction under diverse conditions.

## 📂 Repository Structure

- `rul-predictions-DEM_Bayessian.ipynb`: Main Jupyter notebook implementing the DEM with Bayesian RUL prediction.
- `README.md`: This file.

## 📊 Key Features

- Data preprocessing and normalization pipeline.
- DEM architecture with fixed-point iteration and autograd-based backward pass.
- Training loop with uncertainty estimation using dropout or Bayesian layers.
- Evaluation metrics: RMSE, MAE, uncertainty calibration plots.

## 🛠 Requirements

You can install dependencies with:

```bash
pip install -r requirements.txt
```

Typical dependencies include:
- `torch`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `pandas`
- `tqdm`

You may also optionally use `pytorch-lightning` or `gpytorch` depending on model extensions.

## 🚀 How to Run

1. Clone the repo:
    ```bash
    git clone https://github.com/your-username/rul-dem.git
    cd rul-dem
    ```

2. Open the Jupyter notebook:
    ```bash
    jupyter notebook rul-predictions-DEM_Bayessian.ipynb
    ```

3. Run cells sequentially to preprocess data, train the model, and evaluate results.

## 📈 Results

This model achieves competitive RUL prediction performance on the C-MAPSS dataset and demonstrates calibrated uncertainty estimates, which are critical for safety-critical applications.

## 📄 Citation

If you use this work, please cite:

```bibtex
@Article{electronics14122355,
AUTHOR = {Plakias, Spyridon and Boutalis, Yiannis S.},
TITLE = {A Deep Equilibrium Model for Remaining Useful Life Estimation of Aircraft Engines},
JOURNAL = {Electronics},
VOLUME = {14},
YEAR = {2025},
NUMBER = {12},
ARTICLE-NUMBER = {2355},
URL = {https://www.mdpi.com/2079-9292/14/12/2355},
ISSN = {2079-9292},
ABSTRACT = {Estimating Remaining Useful Life (RUL) is crucial in modern Prognostic and Health Management (PHM) systems providing valuable information for planning the maintenance strategy of critical components in complex systems such as aircraft engines. Deep Learning (DL) models have shown great performance in the accurate prediction of RUL, building hierarchical representations by the stacking of multiple explicit neural layers. In the current research paper, we follow a different approach presenting a Deep Equilibrium Model (DEM) that effectively captures the spatial and temporal information of the sequential sensor. The DEM, which incorporates convolutional layers and a novel dual-input interconnection mechanism to capture sensor information effectively, estimates the degradation representation implicitly as the equilibrium solution of an equation, rather than explicitly computing it through multiple layer passes. The convergence representation of the DEM is estimated by a fixed-point equation solver while the computation of the gradients in the backward pass is made using the Implicit Function Theorem (IFT). The Monte Carlo Dropout (MCD) technique under calibration is the final key component of the framework that enhances regularization and performance providing a confidence interval for each prediction, contributing to a more robust and reliable outcome. Simulation experiments on the widely used NASA Turbofan Jet Engine Data Set show consistent improvements, with the proposed framework offering a competitive alternative for RUL prediction under diverse conditions.},
DOI = {10.3390/electronics14122355}
}
```
