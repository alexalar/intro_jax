    $ cd ~/Documents/source/
    $ git clone git@github.com:alexalar/intro_jax.git

Introduction to JAX
===================
This is an introductory repo for JAX (https://docs.jax.dev/en/latest/index.html)

Getting Started with JAX: https://docs.jax.dev/en/latest/beginner_guide.html#beginner-guide

Make new conda environment
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


Install JAX
-----------------------------

Using JAX requires installing two packages: `jax`, which is pure Python and cross-platform, and `jaxlib` which contains compiled binaries, and requires different builds for different operating systems and accelerators.

-- CPU-only (Linux/macOS/Windows):

    $ conda install jax


-- GPU (NVIDIA, CUDA 12):

    $ pip install -U "jax[cuda12]"


-- GPU (Mac M chips): (Experimental)

Follow: https://developer.apple.com/metal/jax/

    $ pip install jax-metal


Install remaining packages
-----------------------------

    $ conda install matplotlib numpy scipy astropy h5py jupyter nb_conda_kernels
