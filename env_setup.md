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
such as trained models:
```
python -m nltk.downloader punkt
python -m spacy download en_core_web_lg
```

Finally, we can run the [Jupyter Notebook](https://jupyter.org/) to have a web-based environment for writing code 
and creating visualizations.
```
jupyter notebook
```


## Useful links
 - A virtual environment tutorial: https://docs.python.org/3/tutorial/venv.html
 - Jupyter Notebook quickstart: https://jupyter.readthedocs.io/en/latest/content-quickstart.html
 - spaCy quickstart: https://spacy.io/usage/