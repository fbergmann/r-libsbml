## LibSBML R bindings (standalone)
This project contains the R bindings for libSBML, allowing you to work with SBML (Systems Biology Markup Language) files from R.

### Prerequisites

Before building, ensure you have the following dependencies installed:
- CMake (for build configuration)
- SWIG (for generating R bindings)

### Submodules

This project relies on two submodules:
- `libsbml`: Contains the core libSBML library
- `libsbml-dependencies`: Contains required dependencies for libSBML

Make sure to initialize and update the submodules after cloning:

### Checkout

```bash
git clone https://github.com/sbmlteam/r-libsbml
cd r-libsbml
git submodule update --init --recursive --remote
```


### Install
To install the R package, all you'd need is to run: 

```bash
R CMD INSTALL . 
```


### Testing
to test whether installation worked, run one of the examples (from libsbml/examples/r)

```bash
R --slave -f ./libsbml/examples/r/printSupported.R 
```

## Installation on Windows

### Prerequisites
You want to install R, swig and Rtools, either using [winget](https://github.com/microsoft/winget-cli): 

```bash
winget install RProject.R swig rtools
```

or alternatively using [choco](https://chocolatey.org/) from an elevated prompt

```bash
choco install -y rtools R.Project swig
```


then in a Terminal you'll be able to install just as above with: 

```bash
R CMD INSTALL . 
```

and test using

```bash
R --slave -f ./libsbml/examples/r/printSupported.R 
```