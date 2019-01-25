## Introduction

Jupyter notebook provides a web-based application for developing, documenting and executing code.

The main features:
- In-browser code editing
- Displaying of the results of computations in-line
- In-browser editing for rich text using the Markdown markup language
- LaTeX syntax integration

## Installation
To install jupyter in your virtual environment, activate it and type:
```sh
pip3 install jupyter
```

## Running Jupyter

### Locally
To run Jupyter on your local machine, go to a folder you want to create your notebook in and type:
```sh
jupyter notebook
```
This will open a new tab in your browser and display the so-called Notebook Dashboard, where you can manage existing notebooks:
![Notebook Dashboard](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/dashboard.png "Notebook Dashboard")
The Dashboard will only let you see and edit files located only within your startup directory, so make sure to start Jupyter in the correct folder.

### Remotely
Because Jupyter is a server-client-based web application, it is possible to launch it on a remote machine. 
By default, a notebook server starts locally on port `8888` using the same command:
```sh
jupyter notebook
```
You can change the port specifying the `-p` flag as follows:
```sh
jupyter notebook --port <port_number>
```
Once the Jupyter Notebook application is started, you can use SSH tunneling to connect to it.
To establish your own SSH tunnel, run the following command:
```sh
ssh -L 8000:localhost:8888 your_login@your_server_ip
```
Here `8000` is the port on your local machine and `8888` is the port on the remote server where you are running Jupyter.
If one of your local applications is already using the port `8000`, feel free to change it to a different one. 
Once you have forwarded the port, you can copy the URL from your remote server's terminal output and paste it into your browser's address bar.
At this step you should be able to see the Notebook Dashboard.

## Getting started
To create a new notebook, click __New__ at the top right of the Dashboard as in the screenshot:
![New notebook](https://github.com/text-machine-lab/uml_nlp_class_2019/blob/master/screenshots/new_notebook.png "New notebook")

## Interface
The interface of the jupyter notebook is pretty self-explanatory; however, we will cover the main functionality here.
The notebook consists of compuational units called cells, every single cell has either a `Code` or a `Markdown` type. You can switch between the two types by going to `Cell Type` under the `Cell` menu:

You can copy, insert, delete, move and edit cells using the toolbar at the top or using shortcuts.

To execute a single cell, press `Ctrl+Enter`.


For the full documentation please refer to [https://jupyter-notebook.readthedocs.io/en/stable/](https://jupyter-notebook.readthedocs.io/en/stable/)
