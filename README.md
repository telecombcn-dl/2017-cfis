# CFIS WS ML: Lab Exercices

This repository contains several ipython notebooks with machine learning tutorials using python, keras and tensorflow.

## Contents

1. [Installation](#installation)
2. [Setup](#setup)
3. [Sessions](#sessions)
4. [Usage](#usage)


## Installation

- Install git (instructions [here](https://git-scm.com/downloads)).
- Clone this repository ```git clone https://github.com/telecombcn-dl/2017-cfis.git```

### Python

- Linux and MacOSX users: python 2.7 and 3.x are supported. Install from [official website](https://www.python.org/) or use [Anaconda](https://www.continuum.io/downloads)
- Windows users: only Anaconda with python 3.5 is supported (follow detailed steps below).

### Tensorflow

Follow the instructions for your OS to install tensorflow. It is recommended that you install the CPU version of tensorflow, since the GPU version requires cuda and cudnn installed. If you are feeling adventurous and have a GPU, you can follow the instructions in the tensorflow website to do the installation of the GPU version.

#### Linux & Mac OS X

Follow [these instructions](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/g3doc/get_started/os_setup.md#pip-installation) to install tensorflow with pip.

#### Windows

- Install [Anaconda3-4.2.0 X64](https://repo.continuum.io/archive/Anaconda3-4.2.0-Windows-x86_64.exe). It is important that you download this exact version of Anaconda. Otherwise tensorflow installation will likely fail.
- Download and install [Visual C++ 2015 Build Tools](http://landinghub.visualstudio.com/visual-cpp-build-tools).
- Run ```cmd.exe``` as admin.
- Run the following commands:

```shell
conda install conda=4.2.11
conda install jupyter
conda install h5py
conda install scipy
conda create -n tf python=3.5
activate tf
```

- Install Tensorflow:

```
# CPU only
pip install tensorflow
# GPU-enabled
pip install tensorflow-gpu
```

### Other packages

- Install other dependencies ```pip install -r requirements.txt```.
- Set the keras backend to tensorflow in ```~/.keras/keras.json```:

```json
{
    "image_dim_ordering": "tf", 
    "epsilon": 1e-07, 
    "floatx": "float32", 
    "backend": "tensorflow"
}
```

## Setup

Run ``` python setup.py``` to collect datasets and models before we begin, to avoid problems if notebooks freeze at some point.

## Sessions

- [Deep Networks](sessions/deep.ipynb)
- [Convolutional Neural Networks](sessions/convnets.ipynb)
- [Visualization](sessions/visualization.ipynb)
- [Deep Dream](sessions/dream.ipynb)
- [Neural Style](sessions/style.ipynb)


## Usage

All sessions will be run in IPython notebook. To start editing them run:

```shell
jupyter notebook
```

## Deprecated

- [Binary SVM](sessions/binarysvm.ipynb)
