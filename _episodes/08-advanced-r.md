---
title: "Functions in R"
teaching: 30
exercises: 60
questions:
- ""
objectives:
- ""
keypoints:
- ""
---

<!-- MarkdownTOC autolink="True" levels="1,2" -->

- [Introduction](#introduction)
	- [When to make functions?](#when-to-make-functions)
	- [Function trinity](#function-trinity)
- [Scoping](#scoping)
	- [lobal and Local variables](#lobal-and-local-variables)
- [Custom filtering function](#custom-filtering-function)
- [Functionals](#functionals)
- [Split apply combine](#split-apply-combine)
- [List Column Workflow](#list-column-workflow)
	- [References](#references)

<!-- /MarkdownTOC -->

#  Introduction
Functions are at the heart of the R programming language. A lot of analytical steps you will perform in R will be based composed of a series of functions working together.

## When to make functions?
- When you repeat yourself many times. Same block of code repeated over and over (copy-paste-mistake pattern).
- When your code becomes very long (e.g. > 50 lines) and it becomes hard to understand the logic behind your code. What are the steps taken? Why? - - When you need to create a series of plots, models that all differ by very few optional arguments (e.g. p-value threhold), etc. 

## Function trinity    
- Inputs: arguments of your function. This can be accessed using the ?formals(my_function)
- Body: function definition (inside curly braces). What your function does. 
- Environment: 

> ## Exercise
> ```
> subby <- function(a, b) {
>  a - b
> }
> ```
> {: .language-r}
> 
> Type `?formals(subby)`  
> Type `?body(subby)`
> Type `?environment(subby)`
{: .challenge}

# Scoping 

## lobal and Local variables


# Custom filtering function

https://b-rodrigues.github.io/modern_R/defining-your-own-functions.html#functions-that-take-columns-of-data-as-arguments

# Functionals

About the `map` family of functions. Apply a function to a vector or a list. 

[Read and perform the described operations](https://adv-r.hadley.nz/fp.html)


# Split apply combine

[Follow this tutorial](https://burtmonroe.github.io/SoDA501/Materials/SplitApplyCombine_R/)


# List Column Workflow

[Follow this tutorial](https://drsimonj.svbtle.com/running-a-model-on-separate-groups)

## References 

- [Beautiful custom functions in R](https://www.pluralsight.com/guides/beauty-custom-functions-r)