# Visual Studio Code Container Based Environment for Azure CLI

## Prerequisites

- Visual Studio Code Insiders Edition
- Remote - Containers Extension
- Docker

## Using Bare Container

To use container, just run:

	docker run -it --rm zikalino/az

The container contains all the tools and dependencies installed, you can directly run **az** and **azdev**.

Source code is cloned under:

	/workspaces/az/azure-cli
	/workspaces/az/azure-cli-extensions

You may need to do **git pull** to update the source.

## Using in Visual Studio Code (Insiders)

Documentation can be found here:

https://code.visualstudio.com/docs/remote/containers

Clone this repo and clone Azure CLI And Azure CLI Extensions repo:

	git clone https://github.com/zikalino/tools.git
	cd tools/az
	git clone https://github.com/Azure/azure-cli.git
	git clone https://github.com/Azure/azure-cli-extensions.git


Launch Visual Studio Code Insiders from **az** folder:

	code-insiders .

You will be asked if you want to **Reopen in Container**.
Visual Studio Code will perform appropriate setup (only once).
After that is completed you can set a breakpoint and press **F5** to start debugging Azure CLI.