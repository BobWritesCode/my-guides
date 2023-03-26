# Set up VENV

This guides is to help set up a virtual environnement.

This works on my current set up:

- Windows 11
- IDE: Visual Studio Code (VSC)
- Python installed locally (3.10 and 3.11)

## Creating repository folder

- Create a repository folder.
- Open repository folder in IDE.

## Create VENV

- Run these commands in **CMD** terminal in IDE while in repository folder:
  - In **CMD**: `py -m venv VENV_NAME`
    - *example:* `py -m venv venv`

*Tip:* VENV_NAME is venv environment name. `venv` is commonly used.

## Starting VENV

- While in repository folder:
  - If in **CMD** terminal run these commands,
    - `cd venv/Scripts` (Could also be `cd venv/bin`)
    - `activate`
      - Will now see `(venv)` at beginning of file path.
    - `cd ../..`
  - If in **Bash** terminal run these commands,
    - `source venv/Scripts/activate`
      - or if in project directory, if created, toy can use `source ../venv/Scripts/activate`

*Tip:* VENV_NAME is venv environment name from above step.\
*Tip:* Should see (venv) every time hit enter in terminal, to show venv is running.

## Install pip

- While in repository folder:
  - In **CMD** terminal run: `py -m pip install --upgrade pip`

## Install Django in VENV

- While in repository folder:
  - In **CMD** terminal run: `py -m pip install django`

## Install Django REST in VENV

- While in repository folder:
  - In **CMD** terminal run: `py -m pip install djangorestframework`

## Create Django project

- While in repository folder:
  - In **CMD** terminal run: `django-admin startproject PROJECT_NAME`
  - Now change to directory.
  - `cd PROJECT_NAME`

## Running server

- Make sure in project file path.
  - In **CMD** terminal: `py -m manage runserver`

### Tips

`source NAME/bin/activate` example: `source venv/bin/activate` to activate venv\
`pip freeze` to see what is installed.\
`deactivate` to deactivate venv.

## Troubleshoot
