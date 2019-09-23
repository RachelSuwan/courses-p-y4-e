---
title: 'Chapter 3 Conditional Execution'
description: 'Introduction to Boolean Expressions and Logical Operations. We will also cover conditional execution and different kinds of conditionals.'
---

## Boolean Expressions

```yaml
type: PureMultipleChoiceExercise
key: e8330433d0
xp: 50
```

A boolean expression is an expression that is

`@hint`
A boolean is a binary variable, having two states

`@possible_answers`
- right or wrong
- [true or false]
- high or low
- beginning

`@feedback`
- Incorrect
- Correct! A boolean expression is an expression that is either true or false.
- Incorrect
- Incorrect

---

## Passive Command of If Statement

```yaml
type: PureMultipleChoiceExercise
key: 77d0fcb759
xp: 50
```

In an *if statement*, if the logical condition is true, then the indented code gets executed. If the logical condition is false, the indented statement is skipped.
<br>
<b>Which if statement will be executed if x = 10?</b>
	<br>
- if x < 5 :
	<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('Hello')
    <br>
- if x > 10 :
	<br>
	 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('World')
    <br>
- if x < 15 :
	<br> 
	&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('!')

`@hint`
replace x with 10 in each statement, does this make the statement true or false?

`@possible_answers`
- print('Hello')
- print('World')
- [print('!')]

`@feedback`
- Incorrect. x = 10, 10 is not less than 5. This makes the logical condition false, so print('Hello') will not execute
- Incorrect. x = 10, The comparison operator > does not include 10. This makes the logical condition false, so print('World') will not execute
- Correct! x = 10, 10 is less than 15. This makes the logical condition true, so print('!') will execute

---

## Active Command of the If Pattern

```yaml
type: NormalExercise
key: 1b9cfac45c
xp: 100
```

Terry is providing apples to a friend. Her friend needs exactly 8 apples. Help Terry determine if she has enough apples.

`@instructions`
Create 3 If Statements with the variable apples (it has been pre-defined).
1. the first statement should let her know she has not enough apples with output <b>"not enough"</b>
2. the second statement should let her know she has enough apples with output <b>"enough"</b>
3. the third statement should let her know she has more than enough apples with output <b>"more than enough"</b>

`@hint`
1. Create an if statement with the condition that apples are less than 8 and uses the print function to create an output
2. Create an if statement with the condition that apples are equal to 8 and uses the print function to create an output
3. Create an if statement with the condition that apples are greater than 8 and uses the print function to create an output

`@pre_exercise_code`
```{python}
apples = 9
```

`@sample_code`
```{python}

```

`@solution`
```{python}
#statement 1
if apples<8:
  	print('not enough')
#statement 2
if apples==8:
  	print('enough')
#statement 3
if apples>8:
  	print('more than enough')

```

`@sct`
```{python}
#assign if statements
if_statement1 = Ex().check_if_else(0)
if_statement2 = Ex().check_if_else(1)
if_statement3 = Ex().check_if_else(2)

if_statement1.check_test().has_equal_ast()
if_statement1.check_body().has_equal_output()

if_statement2.check_test().has_equal_ast()
if_statement2.check_body().has_equal_output()

if_statement3.check_test().has_equal_ast()
if_statement3.check_body().has_equal_output()

success_msg("Correct! Since apples = 9, Terry has more than enough apples to give to her friend.")

```
