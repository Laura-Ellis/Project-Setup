# How to use this Cookiecutter (once it’s set up)

From any folder:

pip install cookiecutter
cookiecutter path\to\cookiecutter-ds-project


It will ask you things like:

project_name

project_slug

github_username

python_version

Then it will create a new project folder with:

tasks.py

.venv-ready setup

config/colors.py

requirements.template.txt

README.md with TL;DR

PROJECT_SETUP.md

After generation:

cd YOUR_PROJECT_SLUG
python tasks.py create-venv
.venv\Scripts\Activate
python tasks.py install
python tasks.py jupyter

2. Directory structure for the template

Create a folder called e.g. cookiecutter-ds-project, and inside it create this structure:

cookiecutter-ds-project/
  cookiecutter.json
  {{cookiecutter.project_slug}}/
    .gitignore
    README.md
    PROJECT_SETUP.md
    requirements.template.txt
    tasks.py
    config/
      colors.py
    data/
      raw/.gitkeep
      processed/.gitkeep
    notebooks/.gitkeep
    src/.gitkeep
    reports/.gitkeep
