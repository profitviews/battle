# Introduction

This repo is to accompany the [Battle of the Bots](https://profitview.net/battle-of-the-bots) tech sessions for teams. 

The documentation for creating bots can be found [here](https://github.com/profitviews/profitviews/blob/main/docs/signals.md)

**Note:** this repository and associated talks are for educational
purposes only. Nothing contained herein constitutes as investment
advice or offers any advice with respect to the suitability of any
crypto security or trading strategy.

# Getting Started

## 1. Clone this repo

In a suitable directory on your local computer run

```shell
git clone https://github.com/profitviews/battle.git
```

to clone this repository. Ensure you have the [GitHub CLI](https://github.com/cli/cli) installed.

## 2. Install Python 

If you don't already have Python 3.9 or later installed, the recommended way to install Python is by using `pyenv`. Follow the instructions on the [project page](https://github.com/pyenv/pyenv) to install it for your operating system.

Once available, install Python 3.9.15

```shell
pyenv install 3.9.15

pyenv global 3.9.15
```

## 3. Create a `pyenv` virtual environment

The well known package manager [venv](https://docs.python.org/3/library/venv.html) is a bit outdated, so it's recommended to use 
`pyenv-virtualenv` which works with `pyenv`. Follow the instructions on the [project page](https://github.com/pyenv/pyenv-virtualenv) to install it for your operating system.

Once installed create a Python virtual environment to use for this project, and activate it.

```shell
pyenv virtualenv battle

pyenv activate battle
```

## 4. Install the project dependencies

```shell
pip install -r requirements.txt
```

You may get some errors installing the first time round, if you don't have all the non-Python dependencies installed. 

For example TA-Lib is written in C and the Python module is simply a Cython (C-extension) to this main library. The TA-Lib dependencies can be found [here](https://github.com/TA-Lib/ta-lib-python#dependencies).  On Linux follow the [TA-Lib Installation Guide](/TA-Lib-Installation-Guide.md) to install them.

Once all non-Python dependencies are installed re-run the pip install command above, to ensure all libraries are available.

## 5. Run the Jupyter Lab notebook

Now that the dependencies are installed in your virtual environment, you will also need to make the `pyenv` kernel available for Jupyter. 

To do this run the following, with the `workshops` environment activated:

```shell
python -m ipykernel install --user --name=battle
```

If you list the available Jupyter kernels, you should now see this `pyenv` kernel:

```shell
jupyter kernelspec list 
```

Now you will be able to run Jupyter Lab each time by running the following: 

```shell
jupyter lab
```

A new browser tab should open up with the project contents, where you can run the notebook `.ipynb` files from. Note that you will need to select the `workshops` kernel if it is not already selected to ensure that all the dependencies are available in your notebook.

## 6. Follow ups and Help

If you have any issues running anything above, please do not hesistate to reach out either by messaging the dedicated **BitMEX ProfitView Creators** telegram group. We are very happy to help.
