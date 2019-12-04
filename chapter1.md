---
title: 'Chapter 2 - Variables, expression and statements'
description: 'In this module we will be covering the basics of programming languages. With a large focus on values, types, variables and operators. We will also cover the computer uses order of operations to make sense of the code.'
---

## Data Types

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

## Data Types from Variables

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
- [string]
- integer

`@feedback`
- Incorrect. This answer would be correct if the input was not in quotes.
- Correct! If input is ever assigned with quotes, then the input is a string type.
- Incorrect. The input is in quotes and if it wasn't, it is not a whole number.

---

## Using type() to check the type of a variable

```yaml
type: NormalExercise
key: 53889cf984
xp: 100
```

Using the type function to show the type of something.

`@instructions`
>Assign a string, float, and integer to each of the variables. Order does not matter in this case.

`@hint`
- A string must be in quotes and an integer must be a whole number

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
Ex().has_output("<class 'str'>", no_output_msg="Assign a string to the first variable")
Ex().has_output("<class 'float'>", no_output_msg="Assign a float to the second variable")
Ex().has_output("<class 'int'>", no_output_msg="Assign a integer to the third variable")
success_msg("Good Job! As you can see from the output, the console handled each object based on what type of value you assigned to the variable.")
```

---

## Using int(), float(), and str() to convert variables

```yaml
type: NormalExercise
key: e8df7b6d7f
xp: 100
```

Converting variables to different types. Use the int(), float(), and str() methods to convert values to a specific type.

`@instructions`
This is useful for ensuring the proper type is assigned to a variable.
You can either use these methods on the original values being assigned to the variables, or use the functions on the variables themselves and assign the result to the variables.
>Apply these methods in the following order:
- Apply int() to var1
- Apply float() to var2
- Apply str() to var3

`@hint`
- Call the variables inside of the int(), float() and str() methods and reassign to the variables:
- Ex. var1 = int(var1)
- Or you can do this in the original assignment:
- Ex. var1 = int("4.7")

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
var1 = "4"
var2 = "10.89"
var3 = 5
print("Variable 1 = ", var1)
print("Variable 2 = ", var2)
print("Variable 3 = ", var3)
print(type(var1))
print(type(var2))
print(type(var3))
```

`@solution`
```{python}
var1 = int("4")
var2 = float("10.89")
var3 = str(5)
print("Variable 1 = ", var1)
print("Variable 2 = ", var2)
print("Variable 3 = ", var3)
print(type(var1))
print(type(var2))
print(type(var3))
```

`@sct`
```{python}
Ex().check_function('int', missing_msg="Use int() on a variable")
Ex().check_function('float', missing_msg="Use float() on a variable")
Ex().check_function('str', missing_msg="Use str() on a variable")
Ex().has_printout(3, not_printed_msg="Use int() on a variable")
Ex().has_printout(4, not_printed_msg="Use float() on a variable")
Ex().has_printout(5, not_printed_msg="Use str() on a variable")
success_msg("Good Job! These convert nicely, but you cannot convert a string that is not a number. However, you can convert almost anything to a string")
```

---

## Integer Division

```yaml
type: MultipleChoiceExercise
key: 36abdba76e
xp: 50
```

There are two ways to perform division with integers in python. You can use a single slash "/" or a double slash "//". The single will always perform true division and return a floating point number even when division with no remainder. A double slash performs what is called floor division. If you use floor division on a two integers you will get an integer back that is rounded down, if you use it on two floating point numbers it will round down to a whole number.
> What is the result of the following operations? 
Note: You can use the console on your right to test if unsure.
- 5/2
- 5//2
- 10//6

`@possible_answers`
- 3, 2.5, 2
- 2.0, 2, 2
- [2.5, 2, 1]

`@hint`
You can test these by simply putting them into the python console and pressing enter. You will get the solutions.

`@pre_exercise_code`
```{python}

```

`@sct`
```{python}
Ex().has_chosen(correct = 3, # 1-base indexed
msgs = ["That's incorrect.",
		"That's incorrect.",
		"Correct! Head over to the next exercise!"])

```

---

## Rules of Precedence

```yaml
type: MultipleChoiceExercise
key: b535a2a8f5
xp: 50
```

When more than one operator appears in an expression, the order of evaluation depends on the rules of precedence. For mathematical operators, Python follows mathematical convention. The acronym _PEMDAS_ is a useful way to remember the rules:
- Parenthesis
- Exponents
- Multiplication/Division
- Addition/Subtraction


>What are the result of the following equations? Feel free to use the console to test these problems
- 3 ** 2 + 8 * 10
- (5 + 3) * 2 ** 4
- 6 + 4 / 2 * 8

`@possible_answers`
- [89, 128, 22]
 - 170, 128, 40
 - 89, -128, 64

`@hint`
- Parentheses have the highest precedence and can be used to force an expression to evaluate in the order you want. Since expressions in parentheses are evaluated first, 2 * (3-1) is 4, and (1+1) ** (5-2) is 8.
-  Exponentiation has the next highest precedence, so 2 * 1+1 is 3, not 4, and 3 * 1 ** 3 is 3, not 27.
-  Multiplication and Division have the same precedence, which is higher than Addition and Subtraction, which also have the same precedence. So 2 * 3-1 is 5, not 4, and 6+4/2 is 8, not 5.
-  Operators with the same precedence are evaluated from left to right. So the expression 5-3-1 is 1, not 3, because the 5-3 happens first and then 1 is subtracted from 2.

`@pre_exercise_code`
```{python}

```

`@sct`
```{python}
Ex().has_chosen(correct = 1, # 1-base indexed
msgs = ["Correct! Head over to the next exercise!",
		"That's incorrect.",
        "That's incorrect."])
```

---

## Using Commas for Integers

```yaml
type: MultipleChoiceExercise
key: 3f86c48973
xp: 50
```

In this exercise we will be investigating what happens when you use commas for large numbers. Use the console on the right to see how python interprets commas and see what the result of typing this in the console: 1,203,000

`@possible_answers`
- [(1, 203, 0)]
- 1,203,000
- 1203000

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- Use the console to test the number.

`@pre_exercise_code`
```{python}

```

`@sct`
```{python}
# Check https://instructor-support.datacamp.com/en/articles/2375523-course-multiple-choice-with-console-exercises on how to write feedback messages for this exercise.
Ex().has_chosen(correct = 1, # 1-base indexed
msgs = ["Correct! Head over to the next exercise!",
		"That's incorrect.",
        "That's incorrect."])
```

---

## Concatenating Strings

```yaml
type: NormalExercise
key: 7acd5bf8a4
xp: 100
```

Lets say you have two separate strings str1 and str2. str1 is defined as "This is con" and str2 is defined as "catenating strings together". If you want to combine these two strings you can accomplish this through concatenation. You can do this using the + operator with two strings.

`@instructions`
- Create a str3 that is the concatenation of these two strings
- Print str3

`@hint`
- Str3 should look something like String 1 + String 2.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
str1 = "This is con"
str2 = "catenating strings together"
str3 = 
print()
```

`@solution`
```{python}
str1 = "This is con"
str2 = "catenating strings together"
str3 = (str1 + str2)
print(str3)
```

`@sct`
```{python}
Ex().check_object("str3").has_equal_value()
Ex().check_function("print")
success_msg("Good Job!")
```

---

## Taking Input from the User

```yaml
type: PureMultipleChoiceExercise
key: 4de213f542
xp: 50
```

You can use the input() function to obtain input from the user. This can be very useful in many applications and is the fundamental way to interact and obtain information from the user.
- Which of the following calls the input function with context and assigns the result to a variable?

`@hint`
- The string inside of the input function is the context.

`@possible_answers`
- [var = input("This is taking input from the user, type something: ")]
- input("This is taking input from the user, type something: ")
- var = input()

`@feedback`
- Perfect!
- Incorrect.
- Incorrect.

---

## Reserved Words

```yaml
type: MultipleChoiceExercise
key: 439989930c
xp: 50
```

The following are reserved words in python. Reserved words are words that have specific uses and functions in python. Python's interpreter will always use these words as a way to accomplish a specific task:
- and & del & global & not & with
- as & elif & if & or & yield
- assert & else & import  & pass
- break & except & in & raise
- class & finally & is & return
- continue & for & lambda & try
- def & from & nonlocal & while
> Which of the following is a bad use case of reserved words?

`@possible_answers`
- print("and del global")
- [and = 3 + 4]
- if 1: print("hello")

`@hint`
- This goes the same with all programming languages, you should avoid using reserved words for anything other than their purpose at all costs. They should not be used for naming variables or functions.

`@pre_exercise_code`
```{python}

```

`@sct`
```{python}
Ex().has_chosen(correct = 2, # 1-base indexed
msgs = ["That's incorrect.",
        "Correct! Head over to the next exercise!",
        "That's incorrect."])
```

---

## Mnemonic Naming

```yaml
type: PureMultipleChoiceExercise
key: 88deb6c654
xp: 50
```

Programmers use mnemonic naming to allow the programmer to have a easier time understanding and remembering the use of functions. By creating a name that simply identifies the function we are able to read through code and remember what our code does when we create big projects with lots of code and functions. 
- What is an example of both mnemonic and non-mnemonic naming conventions from the following?

`@hint`
- Mnemonic is more specific to the function whereas non-mnemonic is the opposite

`@possible_answers`
- [pizza = print("this is a pizza"); function2 = print("This is a hamburger")]
- function1 = print("this is a pizza"); function2 = print("This is a hamburger")
- pizza = print("this is a pizza"); burger = print("This is a hamburger")

`@feedback`
- That's Correct!
- That is an example of two non-mnemonic names for functions
- That is an example of two mnemonic names for functions

---

## Components of an Assignment Statement

```yaml
type: PureMultipleChoiceExercise
key: e423dea2b7
xp: 50
```

When you create an assignment statement, you are assigning a value to a variable through an operand like an "=". What is the order of the three components of an assignment statement?

`@hint`
- There is a value, a variable and an operand

`@possible_answers`
- value, operand, variable
- name, equals, value
- [variable, operand, value]

`@feedback`
- Incorrect.
- Incorrect.
- Perfect! That concludes chapter 2!
