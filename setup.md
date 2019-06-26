Copyright (c) 2019 OERCompBiomed

# Setting up your system

## Anaconda:
We recommend installing Python via the [Anaconda Distribution](https://www.anaconda.com/download). Be sure to use the "Python 3.6.x" version or later. We will use the Conda Package Management System within the Anaconda Distribution. From the [documentation](https://conda.io/docs):
> Conda is an open source package management system and environment management system that runs on Windows, macOS and Linux. Conda quickly installs, runs and updates packages and their dependencies. Conda easily creates, saves, loads and switches between environments on your local computer.

After the installation run `python --version` in a terminal window (in "Anaconda Prompt" if you are using Windows). If the output show "Python 3.6.x" or later (and "Anaconda") you are good to go.


## Atom:
Atom is a free and open-source text and source code editor for writing and editing text files e.g. YAML configuration files, Markdown files, JSON files, HTML files and others. By its developers it is called a "hackable text editor for the 21st Century" and is a useful tool in addition to the browser-based Jupyter notebook that we will use. Install Atom (Mac Windows Linux) from: https://flight-manual.atom.io/getting-started/sections/installing-atom

## ITK-SNAP:
ITK-SNAP is an open-source image analysis tool used to segment and label structures in 3D medical images. ITK-SNAP is supported on Mac, Windows and Linux and provides semi-automatic segmentation using active contour methods, as well as manual delineation and image navigation. You can read and interact with DICOM and NIFTI images, and plot time-course data. Download the newest release of ITK-SNAP at http://www.itksnap.org/pmwiki/pmwiki.php?n=Downloads.SNAP3

## GitHub:
The course code is hosted on the code-sharing platform GitHub (where you now are reading this). If you do not have a GitHub account already you should make one now. We recommend that you are using the platform for your own projects during the course. https://github.com/join.

## Install and test the course environment:

After you have successfully installed Anaconda, go through the following steps (if you are using Windows, be at the "Anaconda Prompt").

### Install Git:
```bash
conda install git
```
### Download the repository:
```bash
git clone https://github.com/oercompbiomed/Seili-2019
cd Seili-2019
```
### Configure the Python-environment:
```bash
conda env update
```

### Activate the environment:
```bash
conda activate Seili
```
If you are using Linux or MacOS and the command above fails, type
```bash
source ~/.bash_profile
```
and try `conda activate Seili` again. If this fails, activate the environment by typing `source activate Seili` instead.

### Install a Jupyter kernel:
```bash
python -m ipykernel install --user --name Seili --display-name "SEILI"
```

### Install notebook extensions ipywidgets:
```bash
jupyter nbextension enable --py --sys-prefix widgetsnbextension
```

### Test you installation:
Go through the notebook `0.0-test.ipynb` in the `notebooks`-directory:
```bash
cd notebooks
jupyter notebook
```
You can also use [JupyterLab](https://github.com/jupyterlab/jupyterlab): `jupyter lab`.

## Update:
The code and environment will be updated during the course. Run the following commands regularly:
* Update code: `git pull`
* Update environment:
```bash
conda activate Seili
conda env update
```

### Note on Notebooks:

The course is based on the Jupyter Notebook, a web-based framework for developing and presenting code-based projects (take a look at https://youtu.be/HW29067qVWk og https://youtu.be/2eCHD6f_phE for introductions to Jupyter Notebooks).

Throughout the course you will work with notebooks that contain various material and programming tasks. We recommend that you _make a copy of our notebooks before you are editing them_. For the your own version of the notebook you might adopt the naming convention my_[name_of_notebook].ipynb. When running your notebook, remember to change the kernel to SEILI.
