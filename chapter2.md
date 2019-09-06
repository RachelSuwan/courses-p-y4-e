---
title: 'Chapter 2 - Variables, expression and statements'
description: 'In this module we will be covering the basics of programming languages. With a large focus on values, types, variables and operators. We will also cover the computer uses order of operations to make sense of the code.'
---

## 1.1 Data Types

```yaml
type: PureMultipleChoiceExercise
key: 1b28620609
xp: 50
```

Determine the types of the following variables:
1. 3.8
2. 5
3. "4.5"

`@hint`
Anything in quotes will be handled as a string of characters. Integers must be whole numbers.

`@possible_answers`
- string, integer, float
- integer, float, string
- [float, integer, string]

`@feedback`
- Incorrect
- Incorrect
- Correct

---

## 1.2 Data Types from Variables

```yaml
type: PureMultipleChoiceExercise
key: eae0b612d9
xp: 50
```

What is the type of the data assigned to this variable.
variable = '2.3'

`@hint`
The input is in quotes. Input in quotes can only be one type.

`@possible_answers`
- float
- string
- integer

`@feedback`
- Incorrect. This answer would be correct if the input was not in quotes.
- Correct. If input is ever assigned with quotes, then the input is a string type.
- Incorrect. The input is in quotes and if it wasn't, it is not a whole number.

---

## 1.9 Input from User

```yaml
type: NormalExercise
key: 48fd161bd9
xp: 100
```

Creating variables and using the variables

`@instructions`
Use the editor on your right to write python code. 
In this exercise you must assign a value to a variable and print

`@hint`
Put some text in between the two double quotes to create a string that is assigned to variable. 
Then put 'variable' in the print statement

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
#Assign a value to this variable. You can put text in the double quotes or remove double quotes and put a number.
variable = ""
#Put the name of the variable inside the print parentheses to call it in a print statement.
print()
```

`@solution`
```{python}
variable = "This is a string, anything can go here"
print(variable)
```

`@sct`
```{python}
Ex().check_object("variable")
Ex().check_function('print')
success_msg("Good Job!")
```

---

## Insert exercise title here

```yaml
type: NormalExercise
key: 53889cf984
xp: 100
```

Using the type function to show the type of something

`@instructions`
Input a string, float, and integer for variables 1,2,3 respectively.

`@hint`
A string must be in quotes and an integer must be a whole number

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
var1 = 
var2 = 
var3 = 
print(type(var1))
print(type(var2))
print(type(var3))
```

`@solution`
```{python}
var1 = "string"
var2 = 3.4
var3 = 2
print(type(var1))
print(type(var2))
print(type(var3))
```

`@sct`
```{python}
Ex.check_function('type(var1)').has_equal_output(incorrect_msg="Assign a string to the first variable")
Ex.check_function('type(var2)').has_equal_output(incorrect_msg="Assign a float to the second variable")
Ex.check_function('type(var3)').has_equal_output(incorrect_msg="Assign a integer to the third variable")
success_msg("Good Job! As you can see from the output, the console handled each object based on the what you input.")
```
