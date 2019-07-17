# Visual Studio Code Container Based Environment for Azure CLI

## Prerequisites

- Visual Studio Code Insiders Edition
- Extension
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

	git clone 


Clone Azure CLI repositories in this folder:
- azure-cli
- azure-cli-extensions
- azure-cli-dev-tools

Run:

	code-insiders .

in this repository.