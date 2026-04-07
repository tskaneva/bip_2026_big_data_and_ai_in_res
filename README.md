# Erasmus+ BIP "Big Data and AI for the Digitalization of Renewable Energy Systems"

Physical Mobility - 06.04.2026 - 10.04.2026, Ruse Bulgaria
Organizers: 
- Department of Computer Systems and Technologies, University of Ruse, Bulgaria ([cst.uni-ruse.bg]())
- IEEE Student Branch of University of Ruse ([https://sb-ieee.uni-ruse.bg/]()),
- Laboratory "Digital Energy Systems 4.0" ([https://www.facebook.com/profile.php?id=61557608687599]())

## Project Purpose
This repository is part of the Big Data and AI in Renewable Energy Systems workshop and is designed to demonstrate how machine learning techniques can be applied to real-world energy-related problems.

The project focuses on practical use cases such as:
* Solar power forecasting
* Energy price prediction
* Load forecasting
* Renewable energy optimization

The goal is to bridge the gap between theoretical knowledge and practical implementation by providing hands-on examples using real and synthetic datasets.

## Learning Objectives
By working with this repository, you will:

### Understand the ML Workflow
- Data collection  
- Data preprocessing & cleaning  
- Feature engineering  
- Model training  
- Model evaluation  

### Learn Time Series Forecasting
- Working with timestamps  
- Creating lag and rolling features  
- Avoiding data leakage  
- Using chronological train/test splits  

### Work with Real Energy Data
- Weather data  
- PV (solar) generation  
- Electricity load  
- Energy market prices  
- Etc.

### Build Practical Skills
- Python (pandas, NumPy, scikit-learn, matplotlib)  
- Jupyter Notebooks & Google Colab  
- Data visualization and analysis  

### Train and Evaluate Models
- Random Forest  
- Gradient Boosting  
- Baseline models

## Repository Structure
The repository is structured as follows:
```bash
.
├── data/
│ ├── sample_pv_data.csv
│ ├── sample_weather_data.csv
│ └── ...
│
├── workshop notebooks/
│ ├── 01_solar_power_forecasting.ipynb
│ ├── 04_real_data_electricity_price_forecasting_notebook.ipynb
│ └── ...
│
├── datasets/ (optional)
│ └── multi-year real-world datasets
│
├── presentation/
│ └── workshop slides
│
└── README.md
```

### Folder Descriptions

- **`data/`**  
  Sample datasets used in introductory examples. Those datasets are synthetic and not real. Use with caution.

- **`workshop notebooks/`**  
  Main learning materials with step-by-step ML workflows.

- **`datasets/`**  
   Real datasets, used in the 4th workshop example.

- **`presentation`**  
  Workshop slides.

---

## What You Are Expected To Do

This repository is **interactive** — not just for reading.

### Try to:
- Modify features  
- Add new datasets  
- Experiment with different models (e.g. XGBoost, LSTM)  
- Tune hyperparameters  
- Compare results  

Your goal is NOT just to run the code — your goal is to **understand and improve it**

---

## License

This project is intended for **educational and research purposes**.

You are free to:
- Use the code for learning and academic work  
- Modify and extend the examples  

---

## Citation

If you use this repository, please cite:

```
Kaneva, T. (2026).
Big Data and AI in Renewable Energy Systems – Practical Use Cases.
University of Ruse, Bulgaria.
GitHub Repository: https://github.com/tskaneva/bip_2026_big_data_and_ai_in_res
```

---

## Final Note for Students

You are working on **real-world problems** used in modern energy systems.

Don’t worry if:
- your model is not perfect  
- your results are not great

That’s completely normal.

---
# Using Google Colab with Jupyter Notebooks from GitHub

Google Colab lets you open, run, and edit Jupyter notebooks (`.ipynb` files) directly from GitHub — no local setup required.

---

## Prerequisites

- A Google account
- A GitHub account (or access to a public repo, such as this one)
- The GitHub repository URL containing your notebook (copy this URL)

---

## Method 1: Open a Notebook Directly from GitHub

### Option A — Via the Colab Welcome Screen

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. In the welcome dialog, click the **GitHub** tab
3. Paste the GitHub repository URL or search by username
4. Select the notebook (`.ipynb` file) you want to open
5. Click **Open**

### Option B — Modify the GitHub URL Directly

Replace `github.com` with `colab.research.google.com/github` in the URL:

```
# Original GitHub URL:
https://github.com/username/repo/blob/main/notebook.ipynb

# Colab URL:
https://colab.research.google.com/github/username/repo/blob/main/notebook.ipynb
```
## Method 2: Clone the Full Repository into Colab

If you need the entire repo (e.g., for helper scripts, data files, or multiple notebooks), clone it in a Colab code cell:

```python
!git clone https://github.com/username/repo.git
```

Then navigate into the directory:

```python
import os
os.chdir('/content/repo')
```

> ⚠️ **Note:** If you clone the full repository, you might need to update the `BASE_URL` variable in each workbook (usually, step 2).
---

## Saving Changes

Colab does **not** automatically save changes to GitHub. All the changes, you're making are done locally.

---

## Installing Dependencies

If the notebook requires packages not available in Colab by default, install them in a cell:

```python
!pip install package-name
```

Or install from the `requirements.txt` in the repo:

```python
!pip install -r requirements.txt
```

> **Note:** Installations reset when the Colab session ends. Re-run install cells when reconnecting.

---

## Mounting Google Drive (Optional)

To access data files stored in Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

You'll be prompted to authenticate. Files will be available at `/content/drive/MyDrive/`.

---

## Tips & Common Issues

| Issue | Solution                                                 |
|---|----------------------------------------------------------|
| Packages missing after reconnect | Re-run `!pip install` cells                              |
| Changes lost after session | Save to Drive                                            |
| Runtime disconnects | Enable background execution (Pro) or keep tab active     |
| GPU/TPU needed | **Runtime → Change runtime type → Hardware accelerator** |

---

## Quick Reference: Useful Colab Commands

```python
# Check current directory
!pwd

# List files
!ls -la

# Check Python version
!python --version

# Check GPU availability
import tensorflow as tf
print(tf.config.list_physical_devices('GPU'))

# Check available RAM/disk
!df -h
!free -h
```

---

## Resources

- [Google Colab Documentation](https://colab.research.google.com/notebooks/intro.ipynb)
- [GitHub Docs: Personal Access Tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)
- [Colab FAQ](https://research.google.com/colaboratory/faq.html)