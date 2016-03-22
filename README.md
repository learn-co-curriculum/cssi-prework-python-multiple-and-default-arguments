# Multiple and Default Parameters in Python Functions

## Objectives
+ Define and use functions that have multiple parameters
+ Define and use functions that have default arguments
+ Understand the purpose of default arguments in Python

## Overview
We will often want to create and use functions that take in multiple pieces of infomation. For this we add additional parameters during function definition. In other cases, we want to add an argument in only certain situations - we'll create default arguments to solve for these cases.

## Multiple Arguments
Let's say we want to create a function that takes in a user's name, favorite food, and favorite programming language. We can do this by creating our function and separating our parameters using commas within the parentheses:

```python
def long_greeting(name, favorite_food, language):
    return "Hello " + name + ", we have some " + favorite_food + " for you, but first you'll have to write FizzBuzz in " + language + "!"

>>> print long_greeting("Danny", "Lasagna", "Ruby")
Hello Danny, we have some Lasagna for you, but first you'll have to write FizzBuzz in Ruby!
```
Pretty simple - separate multiple parameters using comments. You can use as many parameters as you need.

## Default Arguments

Sometimes it is useful to have a "default" parameter in cases where the user doesn't give us one. For example, I'm building a airfare search function. I'd like the class of seats to default to economy unless otherwise specified:

```python
def airfare_search(start_point, destination, airline_class = "economy"):
    return "searching for " + airline_class + " class tickets from " + start_point + " to " + destination

>>> print airfare_search("New York", "Mumbai", "first")
searching for first class tickets from New York to Mumbai

>>> print airfare_search("Aruba", "Lima")
searching for economy class tickets from Aruba to Lima

```

Notice that I was able to completely omit the airline class in the second invocation of the method, and it defaulted to "economy". This is because we set the default argument in the parameter as `airline_class = "economy"`.

Can you think of situations where you'd need to use default arguments in a function?