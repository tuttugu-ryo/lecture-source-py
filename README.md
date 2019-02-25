
# Lectures in Quantitative Economics Source Files (Python version)

This repository contains 

* the `rst` source files for each python lecture in the [Quantitative Economics](https://lectures.quantecon.org/) in `source/rst`

* supporting code in `source/_static/code/`

* figures, PDFs and other static assets in `source/_static`

You can build and run the lectures as Jupyter notebooks with the help of the [QuantEcon](https://quantecon.org/) built extension [sphinxcontrib.jupyter](https://github.com/QuantEcon/sphinxcontrib-jupyter).


## Installation

1) Download and install [Anacoda](https://www.anaconda.com/distribution/) for your platform (Windows/Linux/Mac OS).

2) Download or clone this repository.

3) Run `make setup`.

The make setup command checks for and installs 

* the [quantecon package](https://pypi.org/project/quantecon/) and 
* the [sphinxcontrib.jupyter extension](https://pypi.org/project/sphinxcontrib-jupyter/) for [Sphinx](https://www.sphinx-doc.org/). 

Other dependencies are included with Anaconda .


## Building notebooks

To transform the `rst` files in to `ipynb` files, run `make notebooks`.

The resulting `ipynb` files are stored in a temporary `_build` directory at the root level of the repository.


## Viewing notebooks

Run `make view`

Additionally you can view a particular lecture directly:

Example `make view lecture=about_py`

The make view command launches a local instance of Jupyter and points it at
the contents of the `_build` directory.


## Workflow

Standard workflow for editing, say, `lqcontrol.rst` is 

1. Run `make notebooks`
1. Run `make view lecture=lqcontrol` to see `lqcontrol.ipynb` in Jupyter
    * or just `make view` and then navigate to `lqcontrol.ipynb` in the browser window that pops up
1.  Edit `lqcontrol.rst` in your favorite text editor 
1. Run `make notebooks` again to 
1. Return to `lqcontrol.ipynb` in Jupyter and reload the page
1. Go to step 3 and repeat as necessary.


