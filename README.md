# PredictingWineFeatures

This project predicts the best features of wines that relate to wine quality. This MLOps pipeline uses a self-managed Digital Ocean Github action-runner, Data Version Control to manage data changes across pipeline stages, and Continuous Machine Learning (CML) to support continual integration metrics analysis of models across stages, experiments, and branches.

## Requirements
* On windows, WSL2, install using the WSL2 instructions, I've got the Ubuntu WSL2 environment installed.
* Python3.x and Pip3 are installed, I have a note in here to alias pip to pip3.
* Docker
* VS Code

## Dataset
Modelling a Kaggle dataset of [red wine properties and quality ratings](https://www.kaggle.com/uciml/red-wine-quality-cortez-et-al-2009).

## Original Project
Original project https://github.com/andronovhopf/wine

## Configure python's VirtualEnv and VSCode
Edit this to the end of ~/.bashrc, save.
~~~
alias pip="pip3"
~~~

### And run these commands to install virtualenv on WSL2
~~~
source ~/.bashrc
pip install virtualenv
~~~

### Validate virtualenv is installed
~~~
virtualenv --version
mkdir ~/.virtualenvs
virtualenv ~/.virtualenvs/PredictWindFeatures
source ~/.virtualenvs/PredictWindFeatures/bin/activate
~~~

### Open VSCode, open the terminal in vscode and run this
~~~
python3 -m virtualenv .virtualenv
~~~

A dialog window will appear in the bottom right corner of VSCode saying the new virtual folder is detected, press "Yes" to use it.
VS Code, install the extension, SonarLint, it will require JRE, let it download and install it. SonarLint will ask to restart VSCode, click "Restart Now".



## Set up Python Requirements and Dependencies
### Now you can run pip installs and they are only installed for your project.
### Install from a requirements.txt document with:

~~~
pip install -r requirements.txt 
~~~

### You can also run "pip freeze" to output the requirements for your python project or to pipe into a requirements.txt to freeze dependency versions.
~~~
pip freeze
~~~