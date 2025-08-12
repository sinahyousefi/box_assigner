# README — How to Run This Jupyter Notebook (No Coding Needed)

This guide shows you, step by step, how to open and run the Jupyter notebook named **main.ipynb** (uses kernel: **Python 3**) — Tested with Python **3.11.2**. You do **not** need to know how to code to follow these steps.

---

## 1) Install Jupyter (one-time)
If you don't have Jupyter yet, install it using **one** of the options below.

**Option 1 — Anaconda (easiest):**
- Download and install **Anaconda** from the official website. During install, accept the defaults.

**Option 2 — Plain Python:**
- Install **Python 3.10 or newer** from python.org.
- After installing, open **Terminal** (macOS) or **Command Prompt** (Windows) and run:
  ```bash
  pip install jupyterlab
  ```

---

## 2) Set up your environment (so everything works)
### Option A (Recommended): Create a clean environment
**Windows & macOS**
1) Open **Terminal** (macOS) or **Command Prompt** (Windows).
2) Go to the folder that contains this notebook:
   ```bash
   cd "/mnt/data"
   ```
3) Choose ONE of the two setup paths below:

   **Path 1 — Anaconda/Miniconda**
   ```bash
   conda create -n myenv python=3.11 -y
   conda activate myenv
   pip install matplotlib numpy pandas scikit-learn
   ```

   **Path 2 — Plain Python**
   ```bash
   python -m venv .venv
   # Windows:
   .venv\Scripts\activate
   # macOS:
   source .venv/bin/activate
   pip install matplotlib numpy pandas scikit-learn
   ```

> If a package fails to install, copy the exact error and share it with your team.

---

## 3) Launch Jupyter
With your environment **activated** (from step 2), start Jupyter:

```bash
jupyter lab
```
or
```bash
jupyter notebook
```

A browser window will open. In the file list, click **main.ipynb** to open it.

---

## 4) Run the notebook
Inside Jupyter:

1. Click **Kernel → Restart & Run All** to run everything from top to bottom, **or** run each cell one by one using the **Run** ▶️ button.
2. If a cell asks for permission or to pick a file, follow the on-screen instructions.
3. Wait for each cell to finish (you'll see a `*` turn into a number like `In [3]`).

### Files the notebook expects to find
- `bags.csv`
- `bags_example.csv`
- `box.csv`

**Tip:** Put these files in the same folder as this notebook (or update the file paths inside the notebook).

---

## 5) What gets installed
If packages are needed, this notebook uses these Python libraries:
- matplotlib
- numpy
- pandas
- scikit-learn

> If you see an error that a package is missing, return to Step 2 and install it with `pip install <package-name>`.

---

## 6) Saving your results
- Your changes are saved automatically as you work.
- Some steps may create new files (for example, `.csv` or `.png`), usually in the same folder as the notebook. Check the left sidebar/file browser in Jupyter.

---

## 7) Troubleshooting (common issues)
- **Jupyter won't open:** Close the window and try running `jupyter lab` again in the same terminal, making sure your environment is activated.
- **Package not found:** Run `pip install <package>` in your active environment, then restart the kernel (`Kernel → Restart`).
- **Kernel error or stuck:** Click `Kernel → Restart` and try **Run All** again.
- **File not found:** Make sure the required files listed above are in the same folder as the notebook, or update the file paths inside the notebook accordingly.
- **Permission denied on macOS:** If macOS blocks the app, go to **System Settings → Privacy & Security** and allow it, then try again.

---

## 8) Need help?
Share a screenshot of the error and the exact step that led to it. That helps your teammate diagnose it quickly.
