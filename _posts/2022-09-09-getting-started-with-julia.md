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
I usually launch Jupyter from within a conda environment in the Terminal. To access Julia from Terminal it needs to be added to the path. Instructions from the [Julia docs] are reproduced here:
```
sudo mkdir -p /usr/local/bin
sudo rm -f /usr/local/bin/julia
sudo ln -s /Applications/Julia-1.8.app/Contents/Resources/julia/bin/julia /usr/local/bin/julia
```

[Julia-download]: https://julialang.org/downloads/
[Julia-docs]: https://julialang.org/downloads/platform/#macos