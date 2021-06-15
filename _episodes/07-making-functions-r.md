---
title: "Functional programming in R"
teaching: 30
exercises: 60
questions:
- "What is the structure of a function in R?"
- "What are functions important for code readability and quality?"
objectives:
- "Understand how a function in R is structured."
- "Be able to name the advantages of creating functions."
- "Be able to execute a vectorised operation using a function and a vector."
keypoints:
- "A function in R consist of a name, one or several arguments, a body and an execution environment."
- "Functions can avoid code repetition and their associated mistake."
- "The name of a function should contain a verb to describe its action."
- "Vectorised operations allow to replace for loops and make your code more readable and maintanable."
---

<!-- MarkdownTOC autolink="True" levels="1,2" -->

- [1. Introduction](#1-introduction)
	- [1.1 When to make functions?](#11-when-to-make-functions)
	- [1.2 Function components](#12-function-components)
	- [1.3 Steps when building a function](#13-steps-when-building-a-function)
- [Good function practices](#good-function-practices)
	- [Use verbs](#use-verbs)
	- [Argument names](#argument-names)
	- [Default arguments](#default-arguments)
- [Scoping](#scoping)
	- [lobal and Local variables](#lobal-and-local-variables)
- [Application to the `gapminder` dataset](#application-to-the-gapminder-dataset)
	- [References](#references)

<!-- /MarkdownTOC -->

#  1. Introduction
Functions are at the heart of the R programming language. A lot of analytical steps you will perform in R will be based composed of a series of functions working together.

## 1.1 When to make functions?
- When you repeat yourself many times. Same block of code repeated over and over (copy-paste-mistake pattern).
- When your code becomes very long (e.g. > 50 lines) and it becomes hard to understand the logic behind your code. What are the steps taken?
- When you want to reuse  code over multiple projects over time. Think about a function that makes a plot from the same type of input data, a functiont that performs unit conversion, etc.
-  Why? - When you need to create a series of plots, models that all differ by very few optional arguments (e.g. p-value threhold), etc. 

## 1.2 Function components    

- __Signature:__ the name of the function together with its arguments. 
- __Arguments:__ arguments of your function. This can be accessed using the `?formals(my_function)` or `?args(my_function)`
- __Body:__ function definition (inside curly braces). What your function does. 
- __Environment:__ the variables and objects in R memory that are known to R inside the function.  


Here is a simple function that converts the _weight in kilograms_ to its corresponding _weight in pounds_. The conversion rate is taken from [Wikipedia](https://en.wikipedia.org/wiki/Avoirdupois_system).   

~~~
convert_kilogram_to_pound <- function(weight_in_kg) {
  # one pound = 0.45359237 kilogram
  # Sourcehttps://en.wikipedia.org/wiki/Avoirdupois_system
  weight_in_pounds <- weight_in_kg / 0.45359237
  return(weight_in_pounds)
}
~~~
{: .language-r}

 
> ## Exercise
> Question 1: Apply the `formals()` function to the `convert_kilogram_to_pound` function. What component of the function do you find?  
> Question 2: What does the `body()` function call on `convert_kilogram_to_pound` return? 
> 
> > ## Solution
> > `formals(convert_kilogram_to_pound)` returns the name(s) of the function arguments. Here it returns `weight_in_kg` as it is the only argument. An alternative function is `formalArgs(convert_kilogram_to_pound)`  which only returns the name of the argument as a character.  
> > `body(convert_kilogram_to_pound)` returns the code written inside the `convert_kilogram_to_pound()` function. 
{: .challenge}

## 1.3 Steps when building a function

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


# Application to the `gapminder` dataset

FIXME: create a plotting function with `country` as an argument. 
FIXME: create a function to calculate the mean, sd and se of different parameters per country with `country` as an argument. 

## References 

- [Beautiful custom functions in R](https://www.pluralsight.com/guides/beauty-custom-functions-r)
- [Richie Cotton DataCamp Introduction to Writing Functions in R](https://learn.datacamp.com/courses/introduction-to-function-writing-in-r)