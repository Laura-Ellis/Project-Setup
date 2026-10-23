# Project-Setup

A Cookiecutter template for data science projects: local virtual environment, simple task runner (`tasks.py`), standard folders, and FAIR files (license, citation, data dictionary, data sources, AI workflow log).

## Create a new project

```bash
pip install cookiecutter
cookiecutter gh:Laura-Ellis/Project-Setup
```

You will be asked for the project name, slug, description, and author details. Defaults are in `cookiecutter.json`.

## What you get

```
my-new-project/
  README.md               portfolio structure: question, summary, data, method, results, AI workflow
  PROJECT_SETUP.md        environment setup steps
  LICENSE                 MIT
  CITATION.cff            citation metadata
  tasks.py                create-venv, install, freeze, jupyter, info
  requirements.template.txt
  config/colors.py
  data/raw/  data/processed/
  data/data_dictionary.csv
  data/DATA_SOURCES.md
  notebooks/  src/
  reports/ai_workflow_log.md
```

Then follow the setup steps below inside the new folder. On macOS or Linux, activate with `source .venv/bin/activate`.

---

# Project Setup – Windows (No Anaconda)

This project uses a local virtual environment (`.venv`) and a simple task runner (`tasks.py`).

# TL;DR:
#### Create virtual environment
```python tasks.py create-venv```
#### Activate (PowerShell)
```.venv\Scripts\Activate```
#### Install dependencies
```python tasks.py install```
#### Launch Jupyter
```python tasks.py jupyter```
#### Update dependencies
```python tasks.py freeze```
#### push to GitHub (after initial commit)
```git remote add origin https://github.com/YOUR_USERNAME/PROJECT_NAME.git
git branch -M main
git push -u origin main
```
#### Recreate environment
```cd PROJECT_NAME
python tasks.py create-venv
python tasks.py install
python tasks.py jupyter```
```
---
# Full version

## 1. Requirements

- Windows
- Python 3.10+ on PATH (`python --version`)
- Git 

---

## 2. Folder Structure

```text
PROJECT_NAME/
  data/
    raw/
    processed/
  notebooks/
  src/
  reports/
  config/
  tasks.py
  requirements.txt        (you create from requirements.template.txt)
  requirements.template.txt
  PROJECT_SETUP.md
  README.md
```

## 3. First-time environment setup (from project root)
```python tasks.py create-venv```

### Create requirements.text (see template)

## 4. Launch jupyter
```jupyter notebook```

## 5. Update dependencies
```python tasks.py freeze```

## 6. Github
```git remote add origin https://github.com/YOUR_USERNAME/PROJECT_NAME.git
git branch -M main
git push -u origin main
```

## 7. to Recreate environment
```cd PROJECT_NAME
python tasks.py create-venv
python tasks.py install
python tasks.py jupyter
```





