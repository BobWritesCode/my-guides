# Set up VENV

This guides is to help set up a virtual environnement. The guide focuses setting up VENV for Django

This works on my current set up:

- Windows 11
- IDE: Visual Studio Code (VSC)
- Python installed locally (3.10 and 3.11)

**IMPORTANT:** I have listed the terminals I have tested the commands in. But just because I tested it in CMD does not mean you cannot do it in BASH.

---

## Table of contents

- [Creating repository folder](#creating-repository-folder)
- [Create VENV](#create-venv)
- [Starting / Activating VENV](#starting--activating-venv)
- [Install pip](#install-pip)
- [Install Django in VENV](#install-django-in-venv)
- [Create Django project](#create-django-project)
- [Create Django app](#create-django-app)
- [Run local Django server](#run-local-django-server)
- [Deactivate VENV](#deactivate-venv)
- [Using commands](#using-commands)

---

## Creating repository folder

- Create a repository folder.
- Open repository folder in IDE.
- In the terminal you should be in `.../repo_folder/`

---

## Create VENV

- Run these commands in **CMD** terminal in IDE while in repository folder:
  - In **CMD**: `py -m venv VENV_NAME`
    - *example:* `py -m venv venv`

*Tip:* `VENV_NAME` is the virtual environment name. `venv` is commonly used.

---

## Starting / Activating VENV

- While in the repository folder (`.../repo_folder/`):
  - If using **CMD** terminal,
    - run: `cd venv/Scripts` (Windows) / `cd venv/bin` (Mac)
    - you should now be in : `.../repo_folder/venv/Scripts` (Windows) / `.../repo_folder/venv/bin` (Mac)
    - run: `activate`
      - You will now see `(venv)` at beginning of file path in the terminal.
    - run: `cd ../..`
    - you should be back in `.../repo_folder/`
  - If using **Bash** terminal,
    - run: `source venv/Scripts/activate`
      - or if in project directory, if created, you can run: `source ../venv/Scripts/activate`

*Tip:* VENV_NAME is venv environment name from above step.\
*Tip:* Should see (venv) every time hit enter in terminal, to show venv is running.

---

## Install pip

- While in repository folder:
  - In **CMD** terminal run: `py -m pip install --upgrade pip`

---

## Install Django in VENV

- While in repository folder:
  - In **CMD** terminal run: `py -m pip install django`

---

## Install Django REST in VENV

**NOTE:** If you are not using Django rest framework, then skip this step.

- While in repository folder:
  - In **CMD** terminal run: `py -m pip install djangorestframework`

---

## Create Django project

- While in repository folder:
  - In **CMD** terminal run: `django-admin startapp app_name`
    - `app_name` is project name of your choice, it can be anything.

---

## Create Django app

- While in Django project directory: `.../repo_folder/project_name`
  - In **BASH** terminal run: `py -m manage startapp app_name`
    - `app_name` is project name of your choice, it can be anything.

---

## Run local Django server

- Make sure you are in your Django project directory: `.../repo_folder/project_name/`.
  - If you are in the repository directory `.../repo_folder/` then do this:
    - In **CMD** terminal run: `cd project_name`
    - You should now be in `.../repo_folder/project_name/`
- In **CMD** terminal run: `py -m manage runserver`

---

## Deactivate VENV

- In **CMD** or **BASH** terminal run: `deactivate` to deactivate venv.

---

## Using commands

How to use commands while in venv.

### **KEY:**

- **(RF)** - While in repo folder `.../repo_folder/`.
- **(PF)** - While in project folder `.../repo_folder/project_name/`.
- **(NA)** - Do not need to be in a specific folder

### **Commands:**

#### Manage.py commands

- **BASH** (PF) either:
  - `py -m manage command`
  - `py manage.py command`
- **CMD** (PF) either:
  - `py -m manage command`
  - `py manage.py command`

#### PIP commands

- **BASH** (NA): `pip command`
- **CMD** (NA): `pip command`

---

## Troubleshoot
