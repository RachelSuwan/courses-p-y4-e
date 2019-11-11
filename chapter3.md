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
Ex().check_function("function1", missing_msg="Make sure function1 is properly defined and called")
Ex().has_output("Hello", incorrect_msg="Make sure the print output is 'Hello')
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
