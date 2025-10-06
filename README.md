# ML4FE:ML Surrogate Models for Finite Element Simulations in Power Electronic Modules' Reliability

This repository uses machine learning methods coupled with finite element simulation results to reduce and optimize computational time. 
<!---
[comment]: [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[comment]: [![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)

[comment]:[cite_start]This repository contains the official source code and data for the paper: **"AI Surrogate Modeling for Lifetime Predictions in Power Electronic Modules"**[cite: 1, 2].

[comment]:[**➡️ Read the Full Paper Here**](./paper/MR_Paper2025_in_progress.pdf)
-->

## Overview 📝
Reliability assesslent of Power Electronic Modules is computationally slow, often relying on the notoriously slow Finite Element Simulations to obtain updates on the mechancial state of the module during its life time. 

This framework introduces: **machine learning surrogate models, replacing slow, high-fidelity simulations.** These surrogates replicate the simulation output with high accuracy while being up to **$10^6$ times faster**, making robust, cycle-by-cycle Remaining Useful Life (RUL) estimation practical.

<!---
[comment]: [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[comment]: [![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/release/python-390/)

[comment]:[cite_start]This repository contains the official source code and data for the paper: **"AI Surrogate Modeling for Lifetime Predictions in Power Electronic Modules"**[cite: 1, 2].

[comment]:[**➡️ Read the Full Paper Here**](./paper/MR_Paper2025_in_progress.pdf)
-->
<!---
[cite_start]Reliability assessment of power electronic modules (PEMs) is often slow and inaccurate, relying on methods that fail to capture non-linear damage accumulation[cite: 9, 10]. [cite_start]Autoregressive models are more robust but are crippled by the high computational cost of the required numerical simulations[cite: 11, 12, 67].

[cite_start]

[cite_start]*A schematic of the proposed autoregressive RUL estimation pipeline enabled by fast surrogate models (see Section 6)[cite: 623].*
-->
## Key contributions ✨

* **Massive Computational Speed-Up:** Achieve a $\approx 10^6$ speed increase over traditional numerical simulations.
* **Comprehensive Model Comparison:** Analysis of various ML families, from Linear Models to Tree-based Ensembles and Neural Networks.
* **Best Practices Guide:** Includes detailed analysis on hyperparameter tuning, residual analysis, feature engineering, and data-size requirements to guide practitioners.
* **Advanced Data Strategy:** Demonstrates the use of Active Learning to intelligently reduce the number of expensive simulations needed for training.
* **Reproducible & Accessible:** All code and data are provided to ensure full reproducibility, designed for practitioners with minimal AI experience.


<!---
## Getting Started 🚀

### 1. Prerequisites

* Python 3.9 or higher
* Conda or another virtual environment manager

### 2. Installation

Clone the repository and install the required dependencies.

```bash
# Clone the repository
git clone [https://github.com/MehdiGhrabli/ML4F.git](https://github.com/MehdiGhrabli/ML4F.git)
cd ML4F

# Create and activate a virtual environment (recommended)
conda create -n ml4f python=3.9
conda activate ml4f

# Install the required packages
pip install -r requirements.txt
```

### 3. Download the Data

The simulation dataset used in the paper is located in the `/data` directory. [cite_start]It consists of 1000 simulation runs, mapping input conditions $(\Delta T, l_c)$ to the total strain field $(\epsilon)$[cite: 209].

### 4. Run the Main Showcase Notebook

To see the core results of the paper, run the main showcase notebook. This will train all the surrogate models and reproduce the performance comparison plots (e.g., Figure 9, 10) from Section 5.

```bash
jupyter notebook notebooks/2_Surrogate_Model_Showcase/2.2_All_Models_Engineered_Features.ipynb
```
-->


## Repository Structure & Workflow

This repository is structured to follow the workflow of the paper.

* **`📄 /paper/`**: Contains the full research paper.
* **`📊 /data/`**: Contains the simulation dataset.
* **`💻 /notebooks/`**: All Jupyter notebooks, organized by task.
    * [cite_start]**`1_Simulation_Data_Validation/`**: Notebooks for validating the numerical simulation setup against experimental data (Appendices B & D)[cite: 701, 802].
    * **`2_Surrogate_Model_Showcase/`**: The main notebooks. [cite_start]Here, we train and evaluate all ML surrogate models, with both original and engineered features, reproducing the core results from Section 5[cite: 306].
    * [cite_start]**`3_Hyperparameter_Tuning/`**: Individual notebooks for performing hyperparameter grid searches for each model family (Section 5.3.1)[cite: 388].
    * **`4_Advanced_Techniques/`**: A demonstration of Active Learning for efficient data acquisition (Section 5.4)[cite: 562].
* **`🛠️ /src/`**: (Optional) Contains helper functions for plotting, data loading, and metrics.

## How to Cite ✒️

If you use this code or the concepts from our paper in your research, please cite us:
### Bibtex
```bibtex
@inproceedings{Ghrabli2025DataDriven,
  author    = "{Ghrabli, Mehdi and Bouarroudj, Mounira and Chamoin, Ludovic and Aldea, Emanuel}",
  title     = "{Data-driven Metamodels for Failure Analysis of Power Electronic Modules}",
  booktitle = "{Proceedings of the 36th European Symposium on Reliability of Electron Devices, Failure Physics and Analysis (ESREF 2025)}",
  year      = "{2025}",
  month     = "{oct}",
  address   = "{Bordeaux, France}",
  note      = "{Forthcoming, to be published on HAL}"
}
```
### APA 
Ghrabli, M., Bouarroudj, M., Chamoin, L., & Aldea, E. (2025). Data-driven metamodels for failure analysis of power electronic modules. In Proceedings of the 36th European Symposium on Reliability of Electron Devices, Failure Physics and Analysis (ESREF 2025). Bordeaux, France.



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
