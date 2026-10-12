# AIoT-2025--TP3 — Logistic Regression on Arduino Uno

Simple, documented solution to [the course TP3](https://github.com/ahmed3991/AIoT-2025/tree/main/TP3).

[Open notebook in Colab](https://colab.research.google.com/github/ggdh17934/AIoT-2025--TP3/blob/main/TP3-Ghanabzia.ipynb)

This repository is **private**. Sign in with your GitHub account when Colab asks
for access. You can also download the notebook and use Colab's **Upload** option.

## Run locally

Use Python 3.11 or newer (TensorFlow builds depend on the supported Python version).
From this project folder:

```sh
python -m pip install -r requirements.txt
python tp3.py
```

## Run the notebook

Run all. The public smoke dataset is downloaded if missing. The notebook trains the two-sensor model and generates src/main.cpp; download that sketch to build in PlatformIO/Wokwi.

The first notebook cell installs missing dependencies. TP2/TP4 also ensure the
versions used for their pickle models. All notebooks contain the actual solution
code; they do not require downloading the Python script just to execute cells.
Saved outputs come from the local run; rerunning generates your own measurements.

## Files

- `TP3-Ghanabzia.ipynb`: notebook with code, outputs, and report display.
- `tp3.py`: Python solution.
- `EXPLICATION_AR.md`: Arabic explanation of the code, concepts and limitations.
- `results/REPORT.md`: measured results and conclusions.
- `results/VALIDATION.md`: what was actually checked.
- `requirements.txt`: runtime dependencies.

## Embedded part

The notebook demonstrates the host-side work. The assignment also requires
`src/main.cpp`, `platformio.ini`, and `diagram.json` for the board/simulator.
Install PlatformIO, open this folder and build:

```sh
pio run -e uno
```

Run the included Wokwi project from VS Code, or upload the sketch to the matching
board. No hardware measurements are invented; see `results/VALIDATION.md` and
GitHub Actions for the actual build status.


## Sources and attribution

Assignment and original wiring: Ahmed Ghenabzia,
[ahmed3991/AIoT-2025](https://github.com/ahmed3991/AIoT-2025).
Solution Python and firmware are implemented for this project; diagrams are
adapted from the course starter files. Smoke data source:
[Kaggle Smoke Detection](https://www.kaggle.com/datasets/deepcontractor/smoke-detection-dataset).
Fashion-MNIST is loaded through the official Keras dataset loader; source:
[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist).
