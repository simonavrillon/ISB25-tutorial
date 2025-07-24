# ISB25-tutorial
Author: Simon Avrillon – Nantes Université

This repository contains a tutorial presented at ISB 2025 demonstrating how to perform EMG signal decomposition using Julia. It includes data preprocessing, decomposition using ICA, and result visualisation.

📦 Requirements

Julia
Python (with the package MNE)
Jupyter notebook

🔧 Installation

1. Install Julia

Download and install Julia from the official website. Add Julia to your system's PATH if needed.

Verify the installation:

julia --version

2. Launch Julia by typing:

julia

In the Julia REPL, run the following:
using Pkg
Pkg.add("IJulia")

This will install the IJulia package and, if Jupyter is not already installed on your system, it will prompt to install it via Conda.

Open the notebook and follow the instructions. You can then run the first cell of the notebook to install all the packages for Julia.

📂 Download the Dataset (BIDS Format)

To run the tutorial, you'll need to manually download five files corresponding to a single EMG contraction, provided in BIDS format:

🔗 Dataset DOI: https://doi.org/10.7910/DVN/L9OQY7

Download the following five files from the dataset:

sub-01_task-isometric30percentmvc_run-01_channels.tsv
sub-01_task-isometric30percentmvc_run-01_coordsystem.json
sub-01_task-isometric30percentmvc_run-01_electrodes.tsv
sub-01_task-isometric30percentmvc_run-01_emg.edf
sub-01_task-isometric30percentmvc_run-01_emg.json

📁 Place these files in the directory data and make sure your full path matches the loading code in the notebook.

🧠 Tutorial Content

The tutorial walks through:

Loading and filtering raw EMG signals
Visualizing EMG channels
Applying fastICA for EMG decomposition
Post-processing and visualisation of motor unit spike trains

tutorial_decomp_ISB2025.ipynb: Main tutorial notebook
data/: Directory containing example EMG data
