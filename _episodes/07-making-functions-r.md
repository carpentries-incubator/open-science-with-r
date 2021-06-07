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
	- [Function components](#function-components)
	- [Steps when building a function](#steps-when-building-a-function)
- [Good function practices](#good-function-practices)
	- [Use verbs](#use-verbs)
	- [Argument names](#argument-names)
	- [Default arguments](#default-arguments)
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
- When your code becomes very long (e.g. > 50 lines) and it becomes hard to understand the logic behind your code. What are the steps taken? Why? - When you need to create a series of plots, models that all differ by very few optional arguments (e.g. p-value threhold), etc. 

## Function components    
- __Arguments:__ arguments of your function. This can be accessed using the `?formals(my_function)` or `?args(my_function)`
- __Body:__ function definition (inside curly braces). What your function does. 
- __Environment:__ the variables and objects in R memory that are known to R inside the function.  

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

## Steps when building a function

1. Making a template: choose a name for your function. Assign it: 
~~~
my_custom_function <- function(){

}
~~~
{: .language-r}

2. Paste the script you already have in your function. 
~~~
my_custom_function <- function(){
	coin_sides <- c("head", "tail")
	flip_times <- 10
	tosses <- sample(coin_sides, size = flip_times, replace = TRUE)
}
~~~
{: .language-r}

3. Choose the arguments of the function. What are the arguments that are likely to change over time?



The `mtcars` is a pre-loaded dataset column descriptions:
- `mpg`: Miles/(US) gallon
- `cyl`: Number of cylinders
- `disp`: Displacement (cu.in.)
- `hp`: Gross horsepower
- `drat`: Rear axle ratio
- `wt`: Weight (1000 lbs)
- `qsec`: 1/4 mile time
- `vs`: V/S
- `am`: Transmission (0 = automatic, 1 = manual)
- `gear`: Number of forward gears
- `carb`: Number of carburetors


> ## Exercise
> Here is a piece of code that returns the median of the miles per gallon (mpg) and the median of the number of cylinders (cyl):
> ~~~
> mtcars 
> ~~~
> {; .language-r}
{: .challenge}

# Good function practices

## Use verbs

Avoid bad naming

`select()` to select column in dplyr. 
`filter()` to filter rows based on 

Readability versus typeability: 
you type code once but you read it multiple it. 
code autocompletion: the long function names can be autocompleted easily within RStudio.  

## Argument names

Data arguments: what you compute on e.g. "mtcars"
Detail arguemnts: how you do the computation e.g. "method = pearson". 

## Default arguments

my_function <- function(x, pvalue = 0.01, na.rm = TRUE)

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