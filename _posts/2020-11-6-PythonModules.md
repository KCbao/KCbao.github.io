---
layout: post
title:  "Python Modules"
date:   2020-10-21 11:18:12 -0700
categories: Python
---

## What is a Python egg?
A Python egg is a structure embodying the release of a specific version of a Python module, comprising its code, resources and metadata. It needs to be **importable** and **discoverable**. 

There are two basic formats currently implemented for Python eggs: 
* `.egg`: a directory or zipfile containing the module's code and resources, along with a `EGG-info` subdirectory that contains the module's metadata
* `.egg-info`: a directory contains module's metadata. 


`.egg` file?

### How to create an egg (`setup.py`)?
To create an .egg file for a directory say mymath which itself may have several python scripts, do the following step
### How to run the egg file?
if you have an .egg file, you can install it as a package using `easy_install`

### `egg-info`?


### `__init__.py`?

## Module not found problem
Sometimes when we type `import <module_1>` at the interactive Python console, we see the following error `ModuleNotFoundError: No module named "<module_1>`. 

__Where does Python look for modules?__

Python looks for modules in `sys.path`. To check `sys.path`, open a Python console, type 
```
import sys
print(sys.path): returns a list of paths
```
To include the module'd directory inside the `sys.path` list, we can use one of the following methods:
1. put the directory into the contents of `PYTHONPATH` environment variable
2. make the module part of an installable package, and install it. 

In the following sections, we discuss in details how to add a directory on the Python `sys.path` list. 

__Methods to add a module__

* Method 1: Append the path to `PYTHONPATH`

`export PYTHONPATH=<path to your package>:$PYTHONPATH`

* Method2: add to .bashrc


## Comments
I encounter this problem twice during my work. First time was I missed to add `__init__.py` in the folder. Second time is that I messed up the folder structure, and I noticed that the package name showed up in the `pip list`, but cause the `Import Error: Module not found` in the python terminal. 

