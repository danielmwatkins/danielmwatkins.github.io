---
title: "Getting started with Julia"
last_modified_at: 2022-09-09
categories:
  - Blog
tags:
  - julia
  - programming
  - scientific computing
---

Julia is a programming language designed for fast scientific computing. It aims to take the readability of Python and Matlab and couple that with the speed of C and Fortran. It also happens to be the language that a key piece of software in my lab is written in, so it's one I need to learn how to use. This post describes how I got up and running with Julia in a Jupyter Notebook on a M1 Mac.

## Installation
Go to the [Julia download page][Julia-download]. Download the one that matches your system. For Mac, installation is as simple as dragging the icon into the applications folder.

## Make Julia accessible from Terminal
I usually launch Jupyter from within a conda environment in the Terminal. To access Julia from Terminal it needs to be added to the path. Instructions from the [Julia docs][Julia-docs] are reproduced here:
```
sudo mkdir -p /usr/local/bin
sudo rm -f /usr/local/bin/julia
sudo ln -s /Applications/Julia-1.8.app/Contents/Resources/julia/bin/julia /usr/local/bin/julia
```

Once you've run that, Terminal should know what you mean when you type `julia`. Go ahead and type that into a Terminal window and you should see:

```
   _       _ _(_)_     |  Documentation: https://docs.julialang.org
  (_)     | (_) (_)    |
   _ _   _| |_  __ _   |  Type "?" for help, "]?" for Pkg help.
  | | | | | | |/ _` |  |
  | | |_| | | | (_| |  |  Version 1.8.0 (2022-08-17)
 _/ |\__'_|_|_|\__'_|  |  Official https://julialang.org/ release
|__/                   |

julia> 
```

## Getting ready for Jupyter
The next step is to add the `IJulia` package so that Jupyter can access the Julia kernel.
The instructions for this are [here][IJulia-docs]. In the same Terminal window where you launched Julia, we'll use the `Pkg` package to install IJulia.

```
using Pkg
Pkg.add("IJulia")
```
For future reference, if Julia gets updated or moved, you'll need to run `Pkg.build("IJulia")` or else it'll stop working. If you already have the Anaconda distribution of Python installed, you're good to go. If not, see the linked IJulia documentation for further instructions.

## Running Julia in a Jupyter notebook
At this point there's little else to do but to open a Jupyter notebook in the usual way: that is, by typing 
```
jupyter notebook
```
in Terminal. Once Jupyter has opened in your browser, you can make a new notebook and you should have Julia as an option in the dropdown menu. 


[Julia-download]: https://julialang.org/downloads/
[Julia-docs]: https://julialang.org/downloads/platform/#macos
[IJulia-docs]: https://julialang.github.io/IJulia.jl/stable/manual/installation/