# Short Exercise: Machine Learning

This repository contains the materials for the short machine learning exercise session prepared for CMSDAS 2026, hosted at USTC in March 2026. The exercises are provided as Jupyter Notebooks.

The goal is to give a hands-on introduction to modern machine learning techniques used in high-energy physics. We start with standard methods like boosted decision trees (BDTs) and deep neural networks (DNNs), and move toward more recent architectures such as Transformers. The exercises begin with a basic classification problem and gradually extend to more realistic HEP use cases.

---

## Getting Started

### Option 1: SWAN

You can open everything directly in SWAN. For environment setup, see `sesh0_intro.pdf`.

[![SWAN](https://swanserver.web.cern.ch/swanserver/images/badge_swan_white_150.png)](https://cern.ch/swanserver/cgi-bin/go/?projurl=https://gitlab.cern.ch/das-hefei2026/exercise.git)

---

### Option 2: lxplus-gpu

1. Log in:

```bash
ssh <USER>@lxplus-gpu.cern.ch
```

2. On the lxplus-gpu node:

```bash
hostname  # e.g. lxplus905.cern.ch

source /cvmfs/sft.cern.ch/lcg/views/LCG_109_cuda/x86_64-el9-gcc13-opt/setup.sh

git clone https://gitlab.cern.ch/das-hefei2026/exercise.git .
cd exercise/Short_exercise/Machine_Learning
jupyter lab --no-browser
```

You will see a link like `http://localhost:8888/lab?token=xxx`. Note the port number (e.g. 8888).

3. On your local machine:

```bash
ssh -L 8888:localhost:8888 <USER>@lxplus905.cern.ch  # change 8888 and lxplus905 as provided above
```

4. Then open the link in your browser.

---

## What's inside

* `sesh0_intro.pdf`
  A quick refresher on basic ML concepts.

* `sesh1_bdt_dnn.ipynb`
  Introduction to BDTs and DNNs.
  You'll train a BDT with XGBoost and a simple DNN with PyTorch for a signal vs. background classification task, and explore how different parameters affect performance.

* `sesh2_transformer.ipynb`
  Using Transformers for classification with token-based inputs (jets/leptons as tokens).
  Focus on understanding the architecture and tuning key hyperparameters.

* `sesh3_tfm_beyond_classif.ipynb`
  Going beyond classification with Transformers in particle physics.
  We look at incorporating physics-inspired features, comparing different inputs, and applying the model to a jet assignment problem.

Each session (1–3) is designed to take about 1.5 hours.

## Exercises

Each session includes a few exercises. Please collect the figures you produce and submit them via [this link](https://cernbox.cern.ch/s/k38RGIHDeErtjQz). We'll showcase selected results after the DAS.

See `hw.md` for details.
