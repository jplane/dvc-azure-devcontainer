# DVC Scenario walkthrus

This devcontainer and set of notebooks captures user scenarios for data management with DVC.

## Prerequisites

- [download](https://www.docker.com/products/docker-desktop/) and install Docker Desktop

- [download](https://code.visualstudio.com/download) and install Visual Studio Code

- [download](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) and install the VS Code Remote Development Extension pack

- you will need an [Azure storage account](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-create?tabs=azure-portal)

## Instructions

1. [create a new blob storage container](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal) in your Azure storage account called 'dvc'

1. [obtain the connection string](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-get-info?tabs=portal#get-a-connection-string-for-the-storage-account) for your storage account

1. open this scenario folder inside VS Code... do not (yet) open inside the devcontainer

1. edit [devcontainer.json](./.devcontainer/devcontainer.json) and add your connection string to line 16

1. now, re-open the scenario folder in VS Code by hitting 'F1' and then selecting 'Dev Containers: Open Folder in Container...' from the command menu

1. once the devcontainer fully builds and opens, open [1-setup.ipynb](/workspace/code/1-setup.ipynb) and execute each cell in order to initialize a local Git repo and DVC

    - you may be prompted to select the local Python kernel prior to execution

1. execute the remaining notebooks in order to see the usage scenarios outlined within
