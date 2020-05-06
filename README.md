# RippleNet

## Description

This repository contains files for RippleNet, a recurrent neural network with LSTM
layers for detecting sharp-wave ripples in single-channel LFP signals measured
in hippocampus CA1.

## Clone

These codes can be downloaded using git (www.git-scm.com):

    cd <Repositories> # whatever download destination
    git clone https://github.com/espenhgn/RippleNet
    cd RippleNet


## dependencies

- `python>=3`
- `numpy`
- `scipy`
- `matplotlib`
- `h5py`
- `pandas`
- `seaborn`
- `notebook`
- `jupyter`
- `tensorflow>=2.0`
- `tensorflow-gpu` (optional)

Dependencies can be installed using the `requirements.txt` file and the `pip` utility:

    pip install -r requirements.txt

To install an Anaconda Python (www.anaconda.com) environment with these dependencies, issue

    conda env create -f conda_environment.yml
    conda activate ripplenet

This will not install `tensorflow-gpu` for hardware acceleration by default.
If you have a pyCUDA capable GPU, go ahead.

## Running

Issue `jupyter-notebook` from the terminal/command line. This should open
an URL in your browser for starting the file `RippleNet_interactive_prototype.ipynb`



## Files and folders:

- `README.md`: This file
- `LICENSE`: License file
- `requirements.txt`: pip requirements file
- `conda_environment.yml`: Conda environment file
- `RippleNet_interactive_prototype.ipynb`: Notebook with interactive rejection of ripple events
- `trained_networks/`
    - `ripplenet_*directional_random_seed*.h5`: trained RippleNet instances of uni- or bidirectional types
    - `ripplenet_*directional_best_random_seed*.h5`: best-performing model on validation set during training
    - `ripplenet_*directional_history_random_seed*.csv`: training history (.csv format)
    - `ripplenet_*directional_history_random_seed*.pkl`: training history (.pickle format)
- `ripplenet/`
    - `common.py`: shared methods and functions
    - `models.py`: function declarations for `tensorflow.keras` models
- `m4029_session1.h5`: Test file
