---
title: 'Chapter 4 - Functions'
description: 'This chapter goes over functions, how they are made, why they are important and some built-in functions'
---

## Defining a Function

```yaml
type: NormalExercise
key: e0c2511b71
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
In this exercise you will learn the following aspects of the functions:
- Using the keyword 'def' to define a function
- Naming a function
- Using parameters
- The body of the function that is called.

`@instructions`
<!-- Guidelines for instructions https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
- Create a function called function1
- Create a parameter for the function
- Have the body print out the parameter.
- Call the function with the parameter "Hello"

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- The first line should like this "def function1 (param1):". Don't forget the colon at the end
- Close the function body with a "return;"
- Tabbing and white space matters, if you put the colon after the parenthesis and hit enter, you should get proper spacing.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
#Here is an example of a function
def DoSomething(parameter):
  #This is the body of the function that is run when the function is called
  print(parameter)
  return;

#Time to call the function with the parameter
DoSomething("This is a parameter")
  
	
```

`@solution`
```{python}
#Here is an example of a function
def function1(param1):
  #This is the body of the function that is run when the function is called
  print(param1)
  return;

#Time to call the function with the parameter
function1("Hello")
```

`@sct`
```{python}
# Examples of good success messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.
Ex().check_function("function1", missing_msg="Make sure function1 is properly defined and called").check_args(0).has_equal_value(incorrect_msg="Make sure the print output is 'Hello'")
success_msg("Good Job! Parameters are optional and you can have more than one or none at all.")
```

---

## Built-in Functions

```yaml
type: NormalExercise
key: 5ea8c2b648
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
In this exercise we will be going over some of the built-in functions in Python.

`@instructions`
<!-- Guidelines for instructions https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
- Use int(), float() and str() to convert the types of variables.
- Use min() and max() on the array, Numbers.
- Put the min and max functions inside of print statements

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- An example of using the type-conversion functions would be "int(Float)"
- An example of using min or max functions would be "max(1, 4, 6)" or "max(Numbers)"

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
#This is a variable with multiple numbers. This is called an array. Use the min() and max() functions on Numbers
Numbers = [4, 5, 2, 4, 8, 31, 10]
#Here are some variable to work with for the type conversions
Str = "5"
Float = 3.2
Int = 2

#These are here to check the new types
print(type(Str))
print(type(Int))
print(type(Float))
```

`@solution`
```{python}
#This is a variable with multiple numbers. This is called an array. Use the min() and max() functions on Numbers
Numbers = [4, 5, 2, 4, 8, 31, 10]
#Here are some variable to work with for the type conversions
Str = "5"
Float = 3.2
Int = 2
int(Float)
str(Int)
float(Str)
#These are here to check the new types
print(type(Str))
print(type(Int))
print(type(Float))
print(min(Numbers))
print(max(Numbers))
```

`@sct`
```{python}
# Examples of good success messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.
Ex().check_function("str", missing_msg="Make sure str() called")
Ex().check_function("int", missing_msg="Make sure int() called")
Ex().check_function("float", missing_msg="Make sure float() called")
Ex().has_output("2", no_output_msg="Make sure to call min() on Numbers inside of a print statement")
Ex().has_output("31", no_output_msg="Make sure to call max() on Numbers inside of a print statement")
success_msg("Good Job! Parameters are optional and you can have more than one or none at all.")
```

---

## Calling Functions

```yaml
type: NormalExercise
key: 7e7386e98a
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
As shown previously, functions must be defined and then called. The calling of a function is exactly what it sounds like. The function is essentially kept in storage and must be called to be used. If you do not call a function after it is defined, it will not be used.

`@instructions`
<!-- Guidelines for instructions https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
- Define two functions named function1 and function2 with printouts "function1" and "function2" respectively
- Parameters are not necessary here.
- Call function1 but not function2.

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- An example of defining a function, "def function_name(parameter_name):"
- If you put a parameter in the definition then it must be called.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}

```

`@solution`
```{python}
def function1():
  print("function1")
  return;
def function2():
  print("function2")
  return;
function1()
```

`@sct`
```{python}
# Examples of good success messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.
Ex().check_function_def("function1", missing_msg="Define function 1")
Ex().check_function_def("function2", missing_msg="Define function 2")
Ex().has_output("function1")
success_msg('Good Job! As you can see from the output, only function1 had its print statement called')
```

---

## Parameters

```yaml
type: NormalExercise
key: 627fdf6786
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
In this exercise, we will show how to work with multiple parameters in a function and demonstrate different ways to call functions.

`@instructions`
<!-- Guidelines for instructions https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
- Call the function provided with the two variables with p1 in param1 and p2 in param2.
- Call it again with the two variables switched.
- Call it one more time with "printFunction(param2 = p1, param1 = p2)"

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- The first call should look like "printFunction(p1, p2)"

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
#Function definition
def printFunction(param1, param2):
  print("This is " + param1)
  print("This is " + param2)
  return;

#Use these variables for ease of use
p1 = "Parameter 1"
p2 = "Parameter 2"


```

`@solution`
```{python}
#Function definition
def printFunction(param1, param2):
  print("This is " + param1)
  print("This is " + param2)
  return;

#Some variables to work with
p1 = "Parameter 1"
p2 = "Parameter 2"

printFunction(p1, p2)
printFunction(p2, p1)
printFunction(param2 = p1, param1 = p2)
```

`@sct`
```{python}
# Examples of good success messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.
Ex().check_function("printFunction", 0).multi(
  check_args(0).has_equal_value(),
  check_args(1).has_equal_value()
)
Ex().check_function("printFunction", 1).multi(
  check_args(0).has_equal_value(),
  check_args(1).has_equal_value()
)
Ex().check_function("printFunction", 2).multi(
  check_args(0).has_equal_value(),
  check_args(1).has_equal_value()
)
success_msg("Good Job! As you can see from this exercise, order matters. When working with lots of parameters it can help to specify which one you are assigning.")
```

---

## Void Functions and Return Statements

```yaml
type: NormalExercise
key: ce0e10604e
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
Up until now, we have only worked with functions that do not return any value after being called. These are called void functions. In this exercise we will look at why returns are important.

`@instructions`
<!-- Guidelines for instructions https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
- Print voidFunction()
- Print returnFunction()

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- Put the function calls within a print statement, or assign the output from each function to a variable and print the variables. Both will work.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
def voidFunction():
  sum1 = 12 + 3
  print("Inside voidFunction: " + str(sum1))
  return;

def returnFunction():
  sum2 = 4 + 5
  print("Inside returnFunction: " + str(sum2))
  return sum2;
```

`@solution`
```{python}
def voidFunction():
  sum1 = 12 + 3
  print("Inside voidFunction: " + str(sum1))
  return;

def returnFunction():
  sum2 = 4 + 5
  print("Inside returnFunction: " + str(sum2))
  return sum2;
  
print(voidFunction())
print(returnFunction())
```

`@sct`
```{python}
# Examples of good success messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.
Ex().check_function("voidFunction")
Ex().check_function("returnFunction")
Ex().has_output("None")
Ex().has_output("9")
success_msg("Good Job! Return functions are very useful and are used just as often as void functions")
```

---

## Why use Functions?

```yaml
type: PureMultipleChoiceExercise
key: ba9c1ddbbb
xp: 50
```

<!-- Guidelines for the question: https://instructor-support.datacamp.com/en/articles/2375516-course-multiple-choice-exercises. -->
In this chapter we have shown how to properly define and use functions. But, we have been applying them to very trivial ideas on a small scale. Here are some things to keep in mind:
- Functions can be very useful to break up large blocks of code into smaller parts. 
- They are also very useful for code that is repeated. If you ever find yourself repeating parts of code, try to use functions instead. 
- A good way to look at libraries in programming languages is as a collection of pre-written functions, classes, values and subroutines that can be called to do a specific task.
- Functions are very useful for coding but don't always need to be used for every bit of code, especially smaller programs.

Which of the following is **NOT** true?

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- Use the text above the question as your guide for below.

`@possible_answers`
- Libraries are just a collection of pre-written functions, classes, values and subroutines.
- Functions are useful for breaking up large blocks of code into smaller chunks.
- [Functions should always be used when you are making a simple and small program.]
- Functions are useful for getting rid of redundant code.

`@feedback`
<!-- Examples of good feedback messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.  -->
- Libraries are in fact made up of pre-written code that can be called like functions.
- Functions make code much more readable because you are routinely naming parts of your code.
- Correct! Functions definitely can be used for small programs, but short programs don't always need functions.
- If you put a redundant piece of code into a function instead, your code will be less lengthy.
