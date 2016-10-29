---
layout:     post
title:      Make Files the Easy way to automate C code compilation
date:       2016-02-20 10:29:19
summary:    Guide on creating and using Make files in C
categories: programming C Make
---

Makefiles are the easy ways to automate code compilation for C files or a bunch of c files
*/
When developing software, a great deal of time (both your own, and CPU time) can be save by using the UNIX utility make.
/*
While developing softwares, a lot of time can be saved using by the utility make.

The idea behind make is that you should be able to compile/link a program simply by typing make (followed by a carriage-return). For this to work, you have to tell the computer how to build your program, by storing instructions in a Makefile.While this step takes some time, you are amply repaid by the time savings later on.

Make is particularly useful for large programs that consist of numerous source files: make only recompiles the file that need recompiling (it works out which ones to process by looking at the dates of last modification).

Here is an example of a simple Makefile:
