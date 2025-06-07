# A Deep Equilibrium Model for Remaining Useful Life of Aircraft Engines

This repository contains the code implementation for the scientific study titled:  
**"A Deep Equilibrium Model for Remaining Useful Life of Aircraft Engines."**

The work presents a novel approach leveraging **Deep Equilibrium Models (DEMs)** for the prediction of **Remaining Useful Life (RUL)** in aircraft engines. It combines fixed-point modeling with Bayesian calibration to handle uncertainty in degradation forecasting.

## 🧠 Overview

- **Deep Equilibrium Models (DEMs)**: A class of implicit-depth models where the output is a fixed point of a learned dynamical system.
- **Bayesian Inference**: Used for uncertainty quantification in RUL prediction.
- **Dataset**: NASA’s C-MAPSS dataset for turbofan engine degradation simulation.

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
@article{your2025deep,
  title={A Deep Equilibrium Model for Remaining Useful Life of Aircraft Engines},
  author={Your Name and Coauthors},
  journal={Journal/Conference Name},
  year={2025}
}
```

## 📬 Contact

For questions or collaborations, please contact:  
**Your Name**  
*Email: your.email@domain.com*
