# Docker container of a library (graph-tool) + VSCode extensions: GitHub Python, Jupyter Notebook, GitHub Copilot 
Tutorial to running a Python library (here: `graph-tool`, which is not available on Windows) in VSCode using Docker containers with extensions: Jupyter Notebooks (inside VSCode) and Github Copilot for fast code completion.

This way, one can use the library on Windows in a container, and keep the benefits of using tools such as GitHub Copilot to develop quicker.


## Quick setup using this repository:

To be added...

## Step-by-step own setup:

Have the **Docker Engine, VSCode**, and the following VSCode **extensions: Docker, Dev Containers + Python, Jupyter Notebook, GitHub Copilot installed**.

### 1) Pull (download) the Docker image of the library of your choice (graph-tool)
Select the Docker image (in my case: *tiagopeixoto/graph-tool*) you want to use, and pull it down. Usually, the maintainer provides the image (sharing its name on the website), or for big enough projects somebody online already has created a Docker image.<br>
You can either pull the image in the command line, like I did:

```docker pull tiagopeixoto/graph-tool```

Or you can open the Docker Engine, search the image and pull it down: 
![image](https://github.com/user-attachments/assets/7ec8e312-df33-4d3f-ab49-38de41272fc7)

Now that you have a Docker image of e.g. the library you want to use, **keep the Docker engine** open.

### VSCode container configurations

Now, we take these steps in VSCode to generate both the Dockerfile, and the devcontainer folder:
- Select a workspace, where you want to have your code (can already put the code in)
- Open your workspace in VSCode, make sure again you have the extensions installed, keep Docker running.
- Press F1 to open the command palette, type *Docker: Add Docker Files to Workspace*, select.
- Set the configurations (e.g. Python, the image, etc.)

VSCode will generate a Dockerfile and other stuff.

This is already enough to run the container, and to use the library in your repository

### Adding more extensions

To add other extensions and not just Python, Jupyter Notebook and GitHub Copilot, extend the down below section in the devcontainer.json file in the .devcontainer folder:

```"customizations": {
        "vscode": {
            "extensions": [
            ...#your extensions
            ]
        }
```

such as this:

![image](https://github.com/user-attachments/assets/892aa77f-2802-4b50-8459-b77050182da4)


## Docker image

Will be added.
