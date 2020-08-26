![](https://images.unsplash.com/photo-1493946740644-2d8a1f1a6aff?ixlib=rb-1.2.1&auto=format&fit=crop&w=1068&q=80)

# Developing inside a Container with Visual Studio Code and Python 

This tutorial walks you through running Visual Studio Code in a Docker container using the Remote - Containers extension. You need no prior knowledge of Docker.

Running VS Code inside a Docker container can be useful for many reasons, but in this walkthrough we'll focus on using a Docker container to set up a development environment that is isolated from your local environment.

[More Info](https://code.visualstudio.com/docs/remote/containers)

# Some WHYs?

With VS Code Remote Containers, the advantages in regards to environment repeatability are massive [link](https://stelligent.com/2020/03/20/development-acceleration-through-vs-code-remote-containers-an-introduction/): 

- Add Repeatability to Your IDE Setup:

        - It is very easy to repeatedly provision the same coding environment in seconds.
        
        - The coding environment itself can easily be adjusted and configured all the while having the benefits of being version controlled alongside the rest of the project.
        
        - Whenever changes are made to the development environment, a developer can rebuild the container to have the newest changes and settings applied.
        
        - It removes any versioning issues that can easily arise from installing items on different machines at different times.
        
- Centralize and Manage VS Code Extensions Seamlessly
- Accelerate Developer Onboarding with Remote Container Setup
- An Agile IDE Strategy

# Prerequisites

You need to fulfil the following prerequisites, to use this feature:

- Install Docker and Docker Compose
- Install Visual Studio Code
- Install the Remote – Container extension

## 1) Install Docker
Docker is needed to create and manage your containers.
Download and install [Docker Desktop](https://www.docker.com/products/docker-desktop). 

## 2) Equinor Managed Laptop

[Follow these instructions.](https://github.com/equinor/edc2019-docker)

## 3) Start Docker
Run the Docker Desktop application to start Docker. You will know it's running if you look in the activity tray and see the Docker whale icon.

Docker might take a few minutes to start. If the whale icon is animated, it is probably still in the process of starting. You can click on the icon to see the status.

## 4) Install Visual Studio Code

## 5) Install the Remote - Containers extension for VS Code
[The Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) lets you run Visual Studio Code inside a Docker container. 

## 6) Clone this github repo on your local machine under your home folder

`git clone https://github.com/baky0905/remote-container-python.git`

## 7) Share the location of your cloned repo(s) with Docker.

Right-click on the Docker task bar item. On Windows, select the Settings menu item then Resources > File Sharing and check the drive(s) where your source code is located. On macOS, select the Preferences menu item then Resources > File Sharing and make sure the folder containing your source code is under a file path specified in the list.

## 8) Open VS Code, CTRL + SHIFT + P and Remote-Containers: Open Folder in Container

The Remote – Container extension provides several ways to develop in a container. You can find more information in the documentation, with several Quick start sections. In this post, I will focus on how to enable this feature for an existing local folder.

As with all the other VS Code extensions, you also manage this with the Command Palette. You can either use the shortcut or the green button in the bottom left corner to open it. In the popup, search for Remote-Containers and select Open Folder in Container…

## For more info on the bigger picture check [this blog post](https://towardsdatascience.com/how-docker-can-help-you-become-a-more-effective-data-scientist-7fc048ef91d5)

```
|   README.md
|
+---.devcontainer
|       .dockerignore
|       devcontainer.json
|       docker-compose.yml # ignore
|       Dockerfile
|       requirements.txt
|
\---src
        analysis_example.ipynb

```

Installed packages:

- adal==1.2.4
- altair==4.1.0
- autopep8==1.5.4
- azure-common==1.1.25
- azure-core==1.8.0
- azure-datalake-store==0.0.49
- azure-identity==1.4.0
- azure-keyvault-certificates==4.2.0
- azure-keyvault-keys==4.2.0
- azure-keyvault-secrets==4.2.0
- azure-keyvault==4.1.0
- azure-storage-blob==12.4.0
- ipykernel==5.3.4
- ipywidgets==7.5.1
- matplotlib==3.2.1
- msal==1.4.3
- nbconvert==5.6.1
- nltk==3.5
- numpy==1.19.1
- pandas-flavor==0.2.0
- pandas==1.1.1
- plotly==4.9.0
- pyjanitor==0.20.9
- pylint
- scikit-learn==0.23.2
- scipy==1.4.1
- seaborn==0.10.1
- urllib3==1.25.10
- xarray==0.16.0
- xlrd==1.2.0

# TODO

Install drivers so that we can consume data from Azure SQL.
