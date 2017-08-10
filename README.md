# Paysage

Paysage is library for unsuperised learning and probabilistic generative models written in Python. The library is still in the early stages and is not yet stable, so new features will be added frequently.

Currently, paysage can be used to train things like:

* Bernoulli Restricted Boltzmann Machines
* Gaussian Restricted Boltzmann Machines
* Hopfield Models

Using advanced mean field and Markov Chain Monte Carlo methods. 

## Physics-inspired machine learning
* **Better performance through better algorithms**. We are focused on making better Monte Carlo samplers, initialization methods, and optimizers that allow you to train Boltzmann machines without emptying your wallet for a new computer.
* **Stay close to Python**. Everybody loves Python, but sometimes it is too slow to get the job done. We want to minimize the amount of computation that gets shifted to the backend by targeting efforts for acceleration to the main bottlenecks in training.


## Installation:
With Anaconda3:
1. Clone this git repo
2. Move into the directory with setup.py
3. Run “pip install -e .”

On MaxOSX with PyEnv:
1. Install pyenv, install python 3.6.0 and set python3 to the python 3.6.0 installation
2. Install llvm 3.9 manually with homebrew
3. Set the LLVM_CONFIG environment variable to the llvm-config file in the llvm 3.9 configuration
4. Clone this git repo
5. Move into the directory with setup.py
6. Run "pip3 install -e ."
7. Make a new file ~/.matplotlib/matplotlibrc with the text "backend: TkAgg". This fixes an issue with importing matplotlib in a virtual enviroment. Check out this [post](http://stackoverflow.com/questions/21784641/installation-issue-with-matplotlib-python) for more information.

Running the examples requires a file mnist.h5 containing the MNIST dataset of handwritten images. The script download_mnist.py in the mnist/ folder will fetch the file from the web.

## Using PyTorch
Paysage uses one of two backends for performing computations. By default, computations are performed using numpy/numexpr/numba on the CPU. If you have installed [PyTorch](http://pytorch.org), then you can switch to the pytorch backend by changing the setting in `paysage/backends/config.json` to `pytorch`. Version 0.2 or greater is required.

## System Dependencies

- hdf5, 1.8 required required by tables
- llvm, llvm-config required by scikit-learn

## About the name:
Boltzmann machines encode information in an ["energy landscape"](https://en.wikipedia.org/wiki/Energy_landscape) where highly probable states have low energy and lowly probable states have high energy. The name "landscape" was already taken, but the French translation "paysage" was not.
