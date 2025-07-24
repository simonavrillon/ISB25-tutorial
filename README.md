# ISB25-tutorial
Author: Simon Avrillon – Nantes Université

This repository contains a tutorial presented at ISB 2025 demonstrating how to perform EMG signal decomposition with Julia. It includes data preprocessing, decomposition using convolutive blind source separation, and result visualisation.

## 📦 Requirements

- Julia
- Python (with the package MNE)
- Jupyter notebook

## 🔧 Installation
0. Setup the project locally

Open the terminal and clone this repository:

```bash
git clone https://github.com/simonavrillon/ISB25-tutorial.git
```
```bash
cd ISB25-tutorial
```

1. Install Julia

Download and install Julia from the [official Julia website](https://julialang.org/downloads/). Add Julia to your system's PATH if needed.

Verify the installation in your terminal:

```bash
julia --version
```

2. Launch Julia by typing:

```bash
julia
```

In the Julia REPL, run the following:

```julia
using Pkg
```
```julia
Pkg.add("IJulia")
```
This will install the IJulia package and, if Jupyter is not already installed on your system, it will prompt to install it via Conda.

3. After installation, you can launch Jupyter Notebook directly from Julia:

```julia
using IJulia
```
```julia
notebook()
```

Alternatively, open the notebook in your IDE with the extensions Julia, Python, and Jupyter installed.

Open the notebook and follow the instructions. You can then run the first cell of the notebook to install all the packages for Julia. It is recommended to install all packages before starting the tutorial, as the installation may take longer than 10 minutes.

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
- Visualising EMG channels
- Applying convolutive blind source separation for EMG decomposition
- Post-processing and visualisation of motor unit spike trains
