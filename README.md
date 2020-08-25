# Developing inside a Container

[More Info](https://code.visualstudio.com/docs/remote/containers)

# Start with a VS Code dev container in just 5 minutes!

Development containers with Visual Studio Code can serve as a fantastic tool in education to ensure colleagues have a consistent coding environment. They take care of setup so that colleagues can quickly move past configuration, and instead focus on what's truly important: learning and coding something great!

#Prerequisites
You need Visual Studio Code installed.

## Install Docker
Docker is needed to create and manage your containers.

## Docker Desktop
Download and install Docker Desktop.

## Start Docker
Run the Docker Desktop application to start Docker. You will know it's running if you look in the activity tray and see the Docker whale icon.

Docker might take a few minutes to start. If the whale icon is animated, it is probably still in the process of starting. You can click on the icon to see the status.

# Install the extension
The Remote - Containers extension lets you run Visual Studio Code inside a Docker container.

# CTRL+SHIF+P

[Install the Remote - Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

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

adal 
altair
autopep8 
azure-datalake-store 
azure-identity 
azure-keyvault 
azure-storage-blob 
chardet 
ipykernel 
ipython 
ipywidgets 
jupyter 
matplotlib 
nbconvert 
nltk 
numpy 
numpy 
pandas 
pandas 
plotly 
pyjanitor 
python-dotenv 
requests 
scikit-learn 
scipy 
seaborn 
urllib3 
wheel 