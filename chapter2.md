---
title: 'Chapter 2 - Variables, expression and statements'
description: 'In this module we will be covering the basics of programming languages. With a large focus on values, types, variables and operators. We will also cover the computer uses order of operations to make sense of the code.'
---

## Types

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

## Intro to Variables

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
