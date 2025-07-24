# ISB25-tutorial
Author: Simon Avrillon – Nantes Université

This repository contains a tutorial presented at ISB 2025 demonstrating how to perform EMG signal decomposition using Julia. It includes data preprocessing, decomposition using convolutive blind source separation, and result visualisation.

## 📦 Requirements

- Julia
- Python (with the package MNE)
- Jupyter notebook

## 🔧 Installation

1. Install Julia

Download and install Julia from the [official Julia website](https://julialang.org/downloads/). Add Julia to your system's PATH if needed.

Verify the installation in your terminal:

<pre>julia --version </pre>

2. Launch Julia by typing:

<pre>julia </pre>

In the Julia REPL, run the following:

<pre>using Pkg

Pkg.add("IJulia") </pre>

This will install the IJulia package and, if Jupyter is not already installed on your system, it will prompt to install it via Conda.

3. After installation, you can launch Jupyter Notebook directly from Julia:

<pre>using IJulia

notebook() </pre>

Open the notebook and follow the instructions. You can then run the first cell of the notebook to install all the packages for Julia.

## 📂 Download the Dataset (BIDS Format)

To run the tutorial, you'll need to manually download five files corresponding to a single EMG contraction, provided in BIDS format:

🔗 Dataset DOI: https://doi.org/10.7910/DVN/L9OQY7

Download the following five files from the dataset:

- sub-01_task-isometric30percentmvc_run-01_channels.tsv
- sub-01_task-isometric30percentmvc_run-01_coordsystem.json
- sub-01_task-isometric30percentmvc_run-01_electrodes.tsv
- sub-01_task-isometric30percentmvc_run-01_emg.edf
- sub-01_task-isometric30percentmvc_run-01_emg.json

📁 Place these files in the directory data and make sure your full path matches the loading code in the notebook.

## 🧠 Tutorial Content

The tutorial walks through:

- Loading and filtering raw EMG signals
- Visualizing EMG channels
- Applying convolutive blind source separation for EMG decomposition
- Post-processing and visualisation of motor unit spike trains
