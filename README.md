Introduction to JAX
===================
This is an introductory repo for JAX

1. Make new conda environment
-----------------------------
Install JAX by creating a fresh `conda` environment. 

As a side note, [`mamba`](https://mamba.readthedocs.io/en/latest/installation/mamba-installation.html) is a fast version of `conda` that uses `conda-forge` as its main channel (this is the channel you should always be using for science work).

With `conda` (`mamba` already does this by default):

$ conda update conda
$ conda config --add channels conda-forge
$ conda config --set channel_priority strict

Make environment:

$ conda create -n jax_intro python=3.12
$ conda activate jax_intro


2. Install JAX
-----------------------------

Using JAX requires installing two packages: `jax`, which is pure Python and cross-platform, and `jaxlib` which contains compiled binaries, and requires different builds for different operating systems and accelerators.

-- CPU-only (Linux/macOS/Windows):

$ pip install -U jax


-- GPU (NVIDIA, CUDA 12):

$ pip install -U "jax[cuda12]"


-- GPU (Mac M chips): (Experimental)

Follow: https://developer.apple.com/metal/jax/

$ pip install -U "jax[cuda12]"


3. Install remaining packages
-----------------------------

$ conda install matplotlib numpy scipy astropy h5py
