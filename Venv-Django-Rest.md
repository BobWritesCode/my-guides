# Set up Virtual Environment (VENV)

This guides is to help set up a virtual environnement. The guide focuses setting up Virtual Environment for Django.

This works on my current set up:

- Windows 11
- IDE: Visual Studio Code (VSC)
- Python installed locally (3.10 and 3.11)

**IMPORTANT:** I have listed the terminals I have tested the commands in. But just because I tested it in CMD does not mean you cannot do it in BASH.

---

## Table of contents

- [Creating repository folder](#creating-repository-folder)
- [Create Virtual Environment](#create-virtual-environment)
- [Starting / Activating Virtual Environment](#starting--activating-virtual-environment)
- [Install pip](#install-pip)
- [Install Django in Virtual Environment](#install-django-in-virtual-environment)
- [Install Django REST in Virtual Environment](#install-django-rest-in-virtual-environment)
- [Creating Django project](#creating-django-project)
- [Creating Django app](#creating-django-app)
- [Run local Django server](#run-local-django-server)
- [Deactivate Virtual Environment](#deactivate-virtual-environment)
- [Using commands](#using-commands)

---

## Creating repository folder

- Create a repository folder.
- Open repository folder in IDE.
- In the terminal you should be in `.../repo_folder/`

---

## Create Virtual Environment

- Run these commands in **CMD** terminal in IDE while in repository folder:
  - In **CMD**: `py -m venv venv_name`
    - *example:* `py -m venv venv`

*Tip:* `venv_name` is the virtual environment name. `venv` is commonly used.

---

## Starting / Activating Virtual Environment

- While in the repository folder (`.../repo_folder/`):
<br/><br/>
  - If using **CMD** terminal,
    - run: `cd venv_name/Scripts` (Windows) / `cd venv_name/bin` (Mac)
      - *example:* `cd venv/Scripts` (Windows) / `cd venv/bin` (Mac)
    - you should now be in : `.../repo_folder/venv_name/Scripts` (Windows) / `.../repo_folder/venv_name/bin` (Mac)
    - run: `activate`
      - You will now see `(venv)` at beginning of file path in the terminal.
    - run: `cd ../..` to back to repo folder (`.../repo_folder/`).
<br/><br/>
  - If using **Bash** terminal,
    - run: `source venv_name/Scripts/activate`
      - *example:* `source venv/Scripts/activate`
    - or if in the project directory (`.../repo_folder/project_name/`), you should run: `source ../venv_name/Scripts/activate`
      - *example:* `source ../venv/Scripts/activate`
<br/><br/>

*Tip:* `venv_name` is virtual environnement name from the [Create VENV](#create-virtual-environment) step.\
*Tip:* Should see `(venv)` every time hit enter in terminal, to show virtual environment is running.

---

## Install pip

- While in repository folder (`.../repo_folder/`):
  - In **CMD** terminal run: `py -m pip install --upgrade pip`

---

## Install Django in Virtual Environment

- While in repository folder (`.../repo_folder/`):
  - In **CMD** terminal run: `py -m pip install django`

---

## Install Django REST in Virtual Environment

**NOTE:** If you are not using Django rest framework, then skip this step.

- While in repository folder (`.../repo_folder/`):
  - In **CMD** terminal run: `py -m pip install djangorestframework`

---

## Creating Django project

- While in repository folder (`.../repo_folder/`):
  - In **CMD** terminal run: `django-admin startproject project_name`
    - `project_name` is project name of your choice, it can be anything.

---

## Creating Django app

- While in Django project directory (`.../repo_folder/project_name/`):
  - In **BASH** / **CMD** terminal run: `py -m manage startapp app_name`
    - `app_name` is project name of your choice, it can be anything.

*Help:* If you are in your repository folder (`.../repo_folder/`) then run: `cd project_name` and you should now be in your project directory (`.../repo_folder/project_name/`)

---

## Run local Django server

- While in Django project directory (`.../repo_folder/project_name/`):
  - In **BASH** / **CMD** terminal run: `py -m manage runserver`

*Help:* If you are in your repository folder (`.../repo_folder/`) then run: `cd project_name` and you should now be in your project directory (`.../repo_folder/project_name/`)

---

## Deactivate Virtual Environment

- In **BASH** / **CMD** terminal run: `deactivate` to deactivate virtual environnement.

---

## Using commands

How to use commands while in virtual environnement.

### **KEY:**

- **(RF)** - While in repo folder (`.../repo_folder/`).
- **(PF)** - While in project folder (`.../repo_folder/project_name/`).
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
