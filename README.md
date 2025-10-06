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

* **Massive Computational Speed-Up:** $\times 10^6$ speed increase over traditional numerical simulations.
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


## Repository Structure 🏗️

This repository is structured as follows.
<!---
* **`📄 /paper/`**: Contains the full research paper.
-->
* **`📊 /data/`**: Contains the simulation dataset.
* **`💻 /code/`**: The Jupyter notebook files used in this project, organized by task.
    * **`Active_Learning/`**: Notebooks for validating the numerical simulation setup against experimental data.
    * **`Hyperparameter_Tuning/`**: Individual notebooks for performing hyperparameter grid searches for each model.
    * **`Surrogate_model_predictions/`**: The main notebooks. Here, we train and evaluate all ML surrogate models, with both original and engineered features, reproducing the core results.
    * **`Validation_for_simulations/`**: Notebooks for validating the numerical simulation setup.
<!--
* **`🛠️ /src/`**: (Optional) Contains helper functions for plotting, data loading, and metrics.
-->

## Getting Started 🚀
### Step 1: Set Up the Environment
This guide is designed to help you get the project running, even if you're new to Python and Jupyter. For scientific projects like this one, setting up Python and all its required libraries can be tricky. Anaconda is a free, all-in-one installation that simplifies this process immensely. It bundles:

*   Python itself.
*   The conda environment manager, which lets us create isolated workspaces for different projects.
*   Key data science libraries, including Jupyter Notebook.

  
By using Anaconda, you get everything you need in a single, straightforward installation, avoiding complex setup issues.

#### Installation Steps

1.  **Install Anaconda:** If you don't have it, download and install the Anaconda Distribution for your operating system.
    * ➡️ **[Anaconda Installation Guide](https://docs.anaconda.com/free/anaconda/install/index.html)**

2.  **Open the Terminal & Navigate:** You'll need to use a command-line interface. On Windows, open the **Anaconda Prompt** from the Start Menu. On macOS or Linux, open the **Terminal**.

3.  **Clone the Repository:** In your terminal, navigate to the directory where you want to store the project (e.g., your Desktop or Documents folder). Use the `cd` (change directory) command, which is the text-based way of opening a folder. Then, clone the repository using this command: 
    ```bash
    # Example: Navigate to your Desktop
    cd Desktop

    # Clone the repository from GitHub
    git clone [https://github.com/MehdiGhrabli/ML4F.git](https://github.com/MehdiGhrabli/ML4F.git)
    ```

6.  **Enter the Project Directory:** Now, move into the newly created project folder.
    ```bash
    cd ML4F
    ```

7.  **Create and Activate the Conda Environment:** This command creates an isolated virtual space named `ml4fe` for this project.
    ```bash
    # Create the environment
    conda create --name ml4fe python=3.9

    # Activate the environment
    conda activate ml4fe
    ```
    Your terminal prompt should now show `(ml4fe)` at the beginning, indicating the environment is active.

8.  **Install Required Libraries:** Finally, install all the necessary Python packages from the `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```

### Step 2: Launch Jupyter Notebook

Now that your environment is set up, you need to make it available inside Jupyter and launch the application.

1.  **Make Your Environment Visible to Jupyter:** Run the following command in your activated `(ml4fe)` terminal. This registers your environment as a "kernel" that Jupyter can use.
    ```bash
    python -m ipykernel install --user --name=ml4fe
    ```

2.  **Start Jupyter Notebook:** Make sure you are still in the `ML4F` project directory in your terminal, then run:
    ```bash
    jupyter notebook
    ```
    This will open a new tab in your web browser showing the project files.

### Step 3: Run the Code

You are now ready to run the project!

1.  **Navigate and Open a Notebook:** In your browser, click on the `code/` directory and select any notebook you wish to run (e.g., `Surrogate_model_predictions/All_Models_Engineered_Features.ipynb`).

2.  **Select the Correct Kernel:** Once the notebook is open, go to the top menu and click **Kernel > Change kernel > ml4fe**. This ensures the notebook uses the environment you just created.

3.  **IMPORTANT - Set the Data Path:** In each notebook, you must tell it where to find the data. Find the cell near the top of the notebook that contains the following line:
    ```python
    # Find this line in the notebook
    Data_sims_file = "C:\\Users\\Mehdi-GHRABLI\\Desktop\\New_Launch\\New_launch_files\\user_files" 
    ```
    Change this placeholder to the correct relative path of the dataset file. Since the notebooks are in `code/`, the path should be:
    ```python
    # Change it to this
    Data_sims_file = "../data/simulation_dataset" 
    ```

4.  **Run the Notebook Cells:** You can now run the cells sequentially by pressing **Shift + Enter** or by using the **Cell > Run All** option in the menu.


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


<!--
## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
-->
