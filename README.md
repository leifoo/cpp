# Notes for book C++ Primer Plus Fifth Edition, Stephen Prata

Play interactively with C++ - Getting Started with Xeus-Cling

https://andersy005.github.io/blog/2018/01/20/play-interactively-with-cpp-getting-started-with-xeus-cling/

1  Getting Started
2  Next: Play interactively with C++ - Streams
xeus-cling

This is the 1st installment of a new series called Play interactively with C++. Every week or so, I’ll be summarizing and exploring Standard C++ Programming in Jupyter notebook using xeus-cling.

The source code (in notebook format) for this series can be found here.

xeus-cling is a Jupyter kernel for C++ based on the C++ interpreter cling and the native implementation of the Jupyter protocol xeus.

In this installment, I will go over how to get started wity toying with C++ Programming interactively.

I am going to show you how to setup your environment. This blog post makes the following assumptions:

The reader has some experience with Jupyter notebooks.
Familiarity with conda.
Note: Credit goes to Uwe for his excellent blog post on how to setup C++ environment for Apache Arrow

Getting Started
To quote xeus-cling project:

It is preferable to install xeus-cling in a fresh conda environment. It is also needed to use a miniconda installation because with anaconda you can have a conflict with the zeromq library which is already installed with anaconda.

As a start, we create a conda environment with all non-C++ dependencies and also install Jupyter Lab from conda-forge.

# Create a new conda environment
conda create -n xeus python=3.6 jupyterlab -c conda-forge
source activate xeus
Finally, let's install the actual interactive environment. For the C++ support, we install the interactive C++ compiler cling and the C++ kernel for Jupyter Notebook xeus-cling from the QuantStack channel.

conda install xeus-cling -c QuantStack -c conda-forge
After starting Jupyter Lab with jupyter lab, you should now see two additional kernels: xeus C++11 and xeus C++14. You can use either of them to use write interactive C++ programs.

The following command hides (base) environment.
conda config --set changeps1 False