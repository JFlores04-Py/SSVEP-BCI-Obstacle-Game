# OpenVEP

## Setup for Windows 11
```
pip install virtualenv
virtualenv pyenv --python=3.11.9
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
pyenv\Scripts\activate
(Install "Desktop development with C++" workload: https://visualstudio.microsoft.com/visual-cpp-build-tools/)
pip install -r requirements.txt
git clone https://github.com/TBC-TJU/brainda.git
cd brainda
pip install -r requirements.txt 
pip install -e .
```
All of the Python packages would be installed into the folder `pyenv/`, so they can be easily removed by simply deleting the folder. When you need to install additional packages, you can activate the virtual environment by running `pyenv\Scripts\activate` and then install the packages using `pip install`. If you want to deactivate the virtual environment, you can run `deactivate`. You may need administrator access to be able to run `pip install -r requirements.txt` successfully.

## Using the rocket game!
```
python run_rocket_syn.py
python scripts/train_trca_rocket.py
(change the run number in run_rocket_syn.py)
```
# 🧠 SSVEP-Based BCI Obstacle Avoidance Game

**Brain-Computer Interface | EEG Signal Processing | Python**

A real-time BCI game that uses Steady-State Visual Evoked Potentials (SSVEPs) to navigate an avatar through an obstacle course. Users focus on flickering stimuli to send directional commands (up, down, left, right, stay) — no physical movement required.

---

## Approach

- **Signal Processing:** Bandpass filtering (1-40 Hz), notch filtering, and Power Spectral Density (PSD) extraction using NumPy/SciPy.
- **Classification:** Logistic Regression (Scikit-learn) trained on PSD features to classify 5-class user attention.
- **Validation:** Permutation testing confirmed statistical significance (p < 0.014).

---

## Results

- **Accuracy:** 40% (chance = 20%, p < 0.014)
- Demonstrated successful real-time BCI control using EEG hardware.

---

## Tools

- **Signal:** NumPy, SciPy, MNE-Python
- **ML:** Scikit-learn (LogisticRegression, StandardScaler)
- **Visualization:** Matplotlib, Seaborn

---

## Quick Start

git clone https://github.com/[your-username]/ssvep-bci-game.git
cd ssvep-bci-game
pip install -r requirements.txt

Run the pipeline:

python src/preprocess.py
python src/train_model.py
python src/run_game.py   # requires live EEG stream

---

## Structure

ssvep-bci-game/
├── data/          # Raw and processed EEG files
├── src/           # Preprocessing, features, model training, game loop
├── results/       # Plots, confusion matrices, exported model
└── requirements.txt

---

## Contact

**Jorge Flores** – george.floresgf2004@gmail.com
GitHub: github.com/[your-username]
LinkedIn: linkedin.com/in/jorge-flores-baa242300
