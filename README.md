# Erasmus+ BIP "Big Data and AI for the Digitalization of Renewable Energy Systems"

Instructions and additional info to be added later.


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