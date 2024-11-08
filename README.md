# SysML v2 Textual Notation Workspace (Kasm Image)

## Introduction

This repo provides a workspace for SysML v2 textual notation modeling based on the [Ansible based template for KASM Ubuntu Focal Images](https://github.com/j-simmons-phd/kasm-core-focal-template) template provided by @j-simmons-phd and upgraded to Ubuntu Noble Numbat manually.  The workspace is configured with the following software:

- git cli 2.47.0
- [Keychain](https://www.funtoo.org/Keychain) 2.8.5
- Chrome
- Python 3.12.x (part of the image template) with the following packages (not part of the image template)
    - pip
    - [JupyterLab](https://jupyter.org/)
    - [Jupyter Notebook](https://jupyter.org/)
    - [Voilà](https://voila.readthedocs.io/en/stable/index.html)
    - [Pint](https://pint.readthedocs.io/en/stable/)
    - [PySysML2](https://github.com/DAF-Digital-Transformation-Office/PySysML2)
- VS Code with the following extensions (note, auto-updates are disabled)
    - [Python extension by Microsoft](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    - [SysIDE CE](https://marketplace.visualstudio.com/items?itemName=sensmetry.sysml-2ls)
- OpenJDK 1.21-75
- GraphViz 2.50.0

## How to Use this Repo

1. Clone this repo, giving the new repo a descriptive name for the workspace image to be created
1. Run `docker-compose pull` to download the image or run `docker-compose build` to build the workspace image 

## Using the image locally

Once built, the image can be pushed into the Kasm server per Kasm documentation or it can be run locally on port 6901 using docker-compose.

- **Starting the image locally:** Run `docker-compose up -d`
- **Stopping the image locally:** Run `docker-compose down`

When running locally, the workspace can be accessed at https://localhost:6901 with
- **User:** `kasm_user`
- **Passwordd:** `password`
