# Setting up development environment

First, we need to create a virtual environment (venv). A virtual environment allows the user  
to install packages without affecting the system interpreter. It is a recommended way for development in python 
as in this case we do not need sudo privileges and can have multiple virtual environments for each of 
the projects, allowing them to have different dependencies.

To create a virtual environment, run the following command:
```
python3 -m venv ~/virt_env/uml_nlp_class_2019
```
`~/virt_env/uml_nlp_class_2019` in the command above is just a path a directory that would be created 
to store your new virtual environment. It can be any path you like.

After we've created the venv, we need to *activate* it. To do it, run 
```
source ~/virt_env/uml_nlp_class_2019/bin/activate
```
Note that the part of the path before `/bin/activate` is the same. In fact, `activate` is 
just a simple bash script that sets some system environment variables (like `PATH`) in order to use 
virtual environment's files.

After we activated the environment, we can install python packages with `pip`. 
```
pip install numpy scikit-learn matplotlib nltk spacy jupyter
``` 

Note that we installed the [scikit-learn](https://scikit-learn.org/stable/) package
for general machine learning algorithms, the [matplotlib](https://matplotlib.org/) package for plotting 
and visualizations, [NLTK](http://www.nltk.org/) and [spaCy](https://spacy.io/) 
for natural language processing algorithms. 

After we installed those packages, we need to download some dependencies for them, 
such as trained models (for example, the spacy `en_core_web_lg` 
[model](https://spacy.io/models/en#en_core_web_lg) contains word vectors and 
trained models for tagging, parsing, and entity recognition:
```
python -m nltk.downloader punkt
python -m spacy download en_core_web_lg
```

Finally, we can run the [Jupyter Notebook](https://jupyter.org/) to have a web-based environment for writing code 
and creating visualizations.
```
jupyter notebook
```

## Jupyter Notebook quick start
Jupyter notebook is a web-based system that allows you to combine 
code, text, and visualizations in a single place. The code is run on a remote 
server, while the editing is happens in your browser. 

Some tips:
 - Enter code into a cell, press `Shift-Enter` to run this cell.
 - You can run cells in an arbitrary order.
 - There can be 'code' cells and 'markdown' cells. 
 Use the menu to change the cell's type.
 - Go to Help -> Keyboard Shortcuts to see available shortcuts.  
   

## Useful links
 - A virtual environment tutorial: https://docs.python.org/3/tutorial/venv.html
 - Jupyter Notebook Introduction: https://nbviewer.jupyter.org/github/jupyter/notebook/blob/master/docs/source/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.ipynb
 - Jupyter Notebook Quickstart: https://jupyter.readthedocs.io/en/latest/content-quickstart.html
 - spaCy quickstart: https://spacy.io/usage/


## Optional: connect to Jupyter remotely
You can setup Jupyter in way so you can connect to it remotely 
from any computer (e.g. from your home). It can be very convenient 
as you don't need to go to the lab to work on a homework.

Since the lab machines are not accessible from the outside network, 
you need to first connect to the cs server (cs.uml.edu) and then connect 
to a lab machine (i.e. da417-01.uml.edu). Moreover, you need to 
forward the Jupyter port (8888) to your local machine. 

Below is an instruction how to achieve this on a Mac or Linux system. 
Windows users can do the same using [putty](https://putty.org/).

Essentially, we need edit the ssh client config file, 
located in your home dir: `~/.ssh/config`. 
This file contains configurations options that are going to be used 
while connecting to a specific server. 
   


