# How the Project Setup Works

(tasks.py • requirements • config)

This project uses three lightweight components to keep setup simple, consistent, and reproducible:

tasks.py — automates environment management

requirements.template.txt / requirements.txt — tracks dependencies

config/ folder — stores reusable project settings (e.g., color palettes)

Below is an explanation of what each one does and how they work together.

tasks.py — Task Runner for Environment Automation

tasks.py replaces long, hard-to-remember setup commands with short, consistent ones.

# What tasks.py does
Command	Description
python tasks.py create-venv	Creates .venv virtual environment
python tasks.py install	Installs packages from requirements.txt
python tasks.py freeze	Saves installed packages → requirements.txt
python tasks.py jupyter	Launches Jupyter Notebook using .venv
python tasks.py info	Shows paths to Python and pip
# Why it exists

Ensures every project uses the same standardized environment setup

Reduces human error (no more manually typing lengthy commands)

Makes the repo fully reproducible for collaborators or future you

Keeps the README small — the automation lives here instead

# Typical workflow using tasks.py
python tasks.py create-venv
.venv\Scripts\Activate
python tasks.py install
python tasks.py jupyter


When you install/remove packages:

pip install PACKAGE_NAME
python tasks.py freeze


This saves updated dependencies to requirements.txt.

# Requirements Files

(requirements.template.txt + requirements.txt)

These files define the Python dependencies needed for your project.

requirements.template.txt

A starter file with categorized packages:

Core (numpy, pandas, pyarrow)

Plotting (matplotlib, seaborn, plotly)

ML (scikit-learn)

NLP (nltk, spacy)

Time series (statsmodels, pmdarima)

Optional extras

You edit this file, delete what you don’t need, and then copy it to:

requirements.txt


The actual list of packages installed into your environment.

Used by:

python tasks.py install


When you make changes to installed packages:

python tasks.py freeze


# This overwrites requirements.txt with the exact set of installed packages.

##  Why this matters

Makes the environment reproducible

Makes GitHub projects self-contained

Ensures Jupyter + scripts all run with the same versions

Supports “works anywhere” portability

# config/ — Reusable Project Settings

This folder holds configuration files your notebooks/scripts import.

Currently includes:

config/colors.py

Contains:

Categorical color palette

Sequential color palette

Category → color mapping

Helper function:

get_category_color("AI/ML")

# Why this matters

Ensures consistent visual style

Keeps color definitions out of notebooks

Central place to update palettes across the entire project

Makes plots and dashboards visually standardized

# Example usage
from config.colors import CATEGORICAL_PALETTE, get_category_color

sns.set_palette(CATEGORICAL_PALETTE)


The config/ folder can later include:

paths.py — shared data paths

params.py — model parameters

theme.py — reusable styling settings

# How These Three Pieces Fit Together
## When starting a new project

Create the folder structure

Create/modify requirements.txt

Run environment setup:

python tasks.py create-venv
python tasks.py install


Launch Jupyter

Import settings from config/

During development

Install a new package

Update requirements:

python tasks.py freeze


Commit changes to Git

## When someone else clones the repo
python tasks.py create-venv
python tasks.py install
python tasks.py jupyter


They now have the exact same environment and project configuration.

# Summary
Component	Purpose
tasks.py	Automates environment creation, installs, freezing, launching Jupyter
requirements.txt	Exact list of dependencies; updated via freeze
requirements.template.txt	Starting point for selecting packages
config/	Contains reusable project-level settings (colors, constants, paths)

These make each project:

Reproducible
Consistent
Easy to set up
Portable
Standardized across your portfolio
