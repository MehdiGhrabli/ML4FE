
# 📁 Dataset

Due to its large size, the dataset for this project is hosted externally on Mega.nz.

You have two options to obtain the data:

1.  **Download the raw simulation output files** (Recommended for full pipeline replication).
2.  **Download the final pre-processed CSV file** (If you want to skip data preparation).

---

## Option 1: Raw Simulation Data (Recommended)

This option allows you to run the entire data pre-treatment code provided in the main repository with minimal changes.

* **Download Link:** **[Download Raw Data](https://mega.nz/file/JiwC2LoY#HmmE5NFRLb0uE4Eg8hBwdO-6M-cUp_C4kfZuvSXsYUo)**
* **Format:** `.zip`

### Description
The zip file contains the raw output from Ansys simulations. It is organized into folders, where each folder represents a specific **Design Point (DP)**.

* **`DPXXXX` Folders**: Each folder (e.g., `DP0001`, `DP0002`) corresponds to a unique simulation run.
* **`.txt` Files**: Inside each `DPXXXX` folder, you will find text files containing:
    * **Simulation Setup**: Input parameters like temperature, crack length, etc.
    * **Simulation Results**: Resulting quantities such as strain and stress at different mechanical nodes `(x, y, z)`.

### Instructions
1.  Download the `.zip` file from the link above.
2.  **Extract its contents directly into this `data` folder.**
3.  After extraction, your `data` folder should look like this:
    ```
    ML4FE/
    ├── data/
    │   ├── DP652/
    │   │   ├── Average_Chip_Temperature.txt
    │   │   └── ...
    │   ├── DP653/
    │   │   └── ...
    │   ├── ...
    │   └── ...
    ├── src/
    └── ...
    ```

---

## Option 2: Pre-processed CSV File

If you wish to skip the data pre-treatment steps and proceed directly to the analysis or model training, you can download the final, consolidated CSV file. This file is the result of running the data processing scripts on the raw data from Option 1.

* **Download Link:** **[Download CSV](https://mega.nz/file/J3ggFYKb#PBUWL1wu7qf8NVUnFFFTf1qmntSJc5dyM91RkxOkuR8)**
* **Format:** `.csv`

### Instructions
1.  Download the `.csv` file from the link above.
2.  Place it directly inside this `data` folder.




