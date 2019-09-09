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

## If Statements

```yaml
type: MultipleChoiceExercise
key: 67eb4e961e
xp: 50
```

In an *if statement*, if the logical condition is true, then the indented code gets executed. If the logical condition is false, the indented statement is skipped.
>Which if statement will be executed if x = 10?
- if x < 5 :
	&nbsp; 
    print('Hello')
- if x > 10 :
	print('World')
- if x < 15 :
	print('!');

`@possible_answers`


`@hint`
Test each 'if' statement in the console window

`@pre_exercise_code`
```{python}
x=10
```

`@sct`
```{python}
Ex().has_chosen(correct=3, msgs= [
  "Incorrect. x = 10, 10 is not less than 5. This makes the logical condition false, so print('Hello') will not execute.",
  "Incorrect. x = 10, The comparison operator > does not include 10. This makes the logical condition false, so print('World') will not execute.",
  "Correct! x = 10, 10 is less than 15. This makes the logical condition true, so print('!') will execute."])
```
