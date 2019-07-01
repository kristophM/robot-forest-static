---
title: "Package Management"
date: 2019-06-23T22:34:01-04:00
draft: true
sort_key: 20
category: "Python"
---
# Package Management in Python

What is a *package*? A package consists of all the files needed for a module to
operate. Analogous to NPM and package.json in JavaScript, and Bundler and Gems in Ruby,
Python manages packages through either *Anaconda.* or *PIP*.

# Anaconda

Anaconda is recommended for data scientists and ML practitioners, because of its
integrated tools for connecting to data sources, collaborating, and deploying
models to production.  

Perhaps one of the biggest differentiators of Anaconda is that it allows you to
set your own environments, each containing different Python versions, and
associated packages that are compatible.

### Install Anaconda

Check if Anaconda has been installed.

```bash
conda --version
```

Download Anaconda at the Anaconda [Download Page](https://www.anaconda.com/distribution/)

## Download a Package Using Anaconda

```bash
conda install seaborn
```

## Use a Package in Your Code

```python
import seaborn
```

## Remove a Package Using Anaconda

```bash
conda remove seaborn
```

## List Installed Packages with Anaconda

```bash
conda list
```

## Updating an Installed Package with Anaconda
```bash
conda update seaborn
```

# PIP

[PIP](https://pypi.org/project/pip/) has been Python's standard package manager for quite a while. It's
good to have PIP around for certain libraries

## Check if PIP is installed

```bash
pip --version
```

If you are on Python 3.4 or above, PIP should automatically be installed.

Otherwise, go to https://pypi.org/project/pip/ and follow the installation instructions.

## Download a Package Using PIP
These get installed on your system.

```bash
pip install seaborn
```

## Use a Package in Your Code

```python
import seaborn
```

## Remove a Package Using PIP

```bash
pip uninstall seaborn
```

## List Installed Packages via PIP
```bash
pip list
```
