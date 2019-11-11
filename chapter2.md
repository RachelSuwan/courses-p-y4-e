---
title: 'Chapter 3 - Conditional Execution'
description: 'Introduction to Boolean Expressions and Logical Operations. We will also cover conditional execution and different kinds of conditionals.'
---

## Boolean Expressions

```yaml
type: PureMultipleChoiceExercise
key: e8330433d0
xp: 50
```

A boolean expression is an expression that is:

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
<b><br><u>Syntax:</u><br>if *condition*:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute if condition is true
<center>![](https://assets.datacamp.com/production/repositories/5344/datasets/cd23b394ceda286212bf220d957c39cd645d00d0/Blank%20Diagram.jpeg)</center>
<br>
><b>Which if statement will be executed if `x = 10?`</b>
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
Create 3 If Statements with the variable apples (apples has been pre-defined).
1. the first statement should let her know she has not enough apples with output <b>"not enough"</b>
2. the second statement should let her know she has enough apples with output <b>"enough"</b>
3. the third statement should let her know she has more than enough apples with output <b>"more than enough"</b>

`@hint`
- Syntax of the if statement consists of a header line that ends with a colon character (:) followed by an indented block.
- Create an if statement with the condition that `apples<8` and uses the `print()` function to create an output
- Create an if statement with the condition that `apples==8` and uses the `print()` function to create an output
- Create an if statement with the condition that `apples>8` and uses the `print()` function to create an output

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
if_statement1 = Ex().check_if_else(0,missing_msg="First if statement not found.")
if_statement2 = Ex().check_if_else(1,missing_msg="Second if statement not found.")
if_statement3 = Ex().check_if_else(2,missing_msg="Third if statement not found.")

if_statement1.check_test().has_equal_ast()
if_statement1.check_body().has_equal_output()

if_statement2.check_test().has_equal_ast()
if_statement2.check_body().has_equal_output()

if_statement3.check_test().has_equal_ast()
if_statement3.check_body().has_equal_output()

success_msg("Correct! Since apples = 9, Terry has more than enough apples to give to her friend.")

```

---

## Passive Command of If Else pattern

```yaml
type: PureMultipleChoiceExercise
key: 0d93b556f0
xp: 50
```

A second form of the *if statement* is <b>alternative execution</b>. Whether the condition is true or false determines which possibility gets executed. One way to express a computation like that is a chained conditional. The alternatives are called branches, because they are branches in the flow of execution.
<b><br><u>Syntax:</u><br>if *condition*:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute if condition is true
<br>else:
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute if condition above is false</b>
  <center>![](https://assets.datacamp.com/production/repositories/5344/datasets/dc5447bef242d317aef551dac9fff72ccfdb5578/Else.jpeg)</center>
<br>
><b>In the following statement, which statement will execute if `x=4?`</b>
	<br>
    <br>
if x != 10 :
	<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the if statement')
    <br>
else:
	<br>
	 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the else statement')
    <br>

`@hint`
-replace x with 4 in the if statement, does this make the statement true or false?

`@possible_answers`
- The if statement
- [The else statement]
- Neither will execute

`@feedback`
- Incorrect. The else statement will execute only if `x=10`.
- Correct! Since x=9, it does not equal 10. Thus, making the statement `x!=10` true. The if statement executes.
- Incorrect. One of these statements will execute if `x=4`.

---

## Active Command of If Else

```yaml
type: NormalExercise
key: f23ee953dd
xp: 100
```

Terry is providing apples to a friend. Her friend needs exactly 8 apples. Help Terry determine if she has enough apples.

`@instructions`
Create an if-else statement with the variable apples (apples has been pre-defined).
1. The condition for the if statement should check if apples equals 8, and notify <b>"enough apples"</b>
2. The else statement should notify <b>"not enough or too many"</b>

`@hint`
- Syntax of an if-else statement consists of:
<br>1. an `if` header line that ends with a colon character (:) followed by an indented block
<br>2. an `else` header line that ends with a colon character (:) followed by an indented block
- Create an if statement with the condition that apples==8 and uses the` print()` function to notify "enough apples"
- Create an else statement that uses the `print()` function to notify "not enough or too many"

`@pre_exercise_code`
```{python}
apples = 20
```

`@sample_code`
```{python}

```

`@solution`
```{python}
if apples == 8:
  	print("enough apples")
else:
	print("not enough or too many")
```

`@sct`
```{python}
#assign if statements
if_statement = Ex().check_if_else(0,missing_msg="if statement not found.")

if_statement.check_test().has_equal_ast()
if_statement.check_body().has_equal_output()
if_statement.check_orelse().has_equal_output()
success_msg("Correct! Since apples = 20, the else statement executes.")
```

---

## Passive Command of the if elif pattern

```yaml
type: PureMultipleChoiceExercise
key: 794c390943
xp: 50
```

Sometimes there are more than two possibilities and we need more than two branches. One way to express a computation like that is a chained conditional. An *elif statement*, an abbreviation of “else if”, is a chained conditional that handles more than two branches. There is no limit to the number of elif statements and an else statement is not required to follow. 
<b><br><u>Syntax:</u><br>if *condition*:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute if first condition is true
<br>elif *condition*:
      <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute if first condition is false and second condition is true
<br>else:
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Default statement block to execute if all conditions above are false</b>
  <center>![](https://assets.datacamp.com/production/repositories/5344/datasets/d2881a9a5d9452951ac180cca33b7c668f39d57f/Elif.jpeg)</center>
<br>
>Which of the following displays proper `elif` syntax?

`@hint`
There is no limit to the number of `elif` statements. An `else` statement will go <b>after</b> any `elif` statements however, an `else` statement is not mandatory.

`@possible_answers`
- if x==2:
<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the if statement')
<br>
else:
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the else statement')
<br>
- if x==2:
<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the if statement')
<br>
else:
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the else statement')
<br>
elif x==4:
<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the else statement')
<br>
- [if x==2: <br>    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the if statement')<br>elif x==4:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in the elif statement')<br>elif x==6:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;print('This is in another elif statement')<br>]

`@feedback`
- Incorrect. This is correct syntax for an if-else statement, not an elif statement.
- Incorrect. The elif statement must come before the else statement.
- Correct!

---

## Active Command of the if elif pattern

```yaml
type: NormalExercise
key: a0a270e308
xp: 100
```

Terry is providing apples to a friend. Her friend needs exactly 8 apples. Help Terry determine if she has enough apples.

`@instructions`
Create an if-elif-else statement with the variable apples (apples has been pre-defined).
1. the `if statement` should let her know she has exactly enough apples with output <b>"exactly 8 apples"</b>
2. the `elif statement` should let her know she does not have enough apples with output <b>"not enough"</b>
3. the `else statement` should let her know she has more than enough apples with output <b>"more than enough"</b>

`@hint`
- Syntax of an if-elif statement consists of:
<br>1. an `if` header line that ends with a colon character (:) followed by an indented block
<br>2. an `elif` header line that ends with a colon character (:) followed by an indented block
<br>3. an `else` header line that ends with a colon character (:) followed by an indented block
- Create an if statement with the condition that apples==8 and uses the` print()` function to notify "exactly 8 apples"
- Create an elif statement with the condition that apples<8 that uses the `print()` function to notify "not enough"
- Create an else statement that uses the `print()` function to notify "more than enough"

`@pre_exercise_code`
```{python}
apples = 4
```

`@sample_code`
```{python}

```

`@solution`
```{python}
if apples == 8:
  print("exactly 8 apples")
elif apples < 8:
  print("not enough apples")
else:
  print("more than enough ")
```

`@sct`
```{python}
#assign if statements
#elif-else SCT

Ex().check_if_else().multi(
    check_test().has_equal_ast(),          # zoom in on apples == 8
    check_body().has_equal_output(),          # zoom in on print("exactly 8 apples")
    check_orelse().check_if_else().multi(
        check_test().has_equal_ast(),      # zoom in on apples < 8
        check_body().has_equal_output(),      # zoom in on print("not enough apples")
        check_orelse().has_equal_output()     # zoom in on print('more than enough')
    )
)
success_msg("Correct! Since apples = 4, Terry does not have enough apples to give to her friend.")

```

---

## Passive command of Nested Loops

```yaml
type: PureMultipleChoiceExercise
key: 1e4c0f9c28
xp: 50
```

<!-- Guidelines for the question: https://instructor-support.datacamp.com/en/articles/2375516-course-multiple-choice-exercises. -->

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- This is an example hint.
- This is an example hint.

`@possible_answers`
- [Correct answer 1]
- Wrong answer 2
- Wrong answer 3

`@feedback`
<!-- Examples of good feedback messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.  -->
- Perfect!
- Error message answer 2
- Error message answer 3

---

## Passive Try Except

```yaml
type: PureMultipleChoiceExercise
key: ab9f768191
xp: 50
```

Input from a user can potentially cause errors. A conditional execution structure that handles both expected and unexpected errors is called try/except. The try block tries a statement that may have issues, the except is executed if an error occurs in the statement and is ignored if there are no errors. 
<b><br><u>Syntax:</u><br>try:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute
<br>except:
  <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Indented statement block to execute if condition above has an error</b>

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- This is an example hint.
- This is an example hint.

`@possible_answers`
- [Correct answer 1]
- Wrong answer 2
- Wrong answer 3

`@feedback`
<!-- Examples of good feedback messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.  -->
- Perfect!
- Error message answer 2
- Error message answer 3

---

## Active Try Except

```yaml
type: NormalExercise
key: 7e8c31a99b
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->

`@instructions`
<!-- Guidelines for instructions https://instructor-support.datacamp.com/en/articles/2375526-course-coding-exercises. -->
- Instruction 1
- Instruction 2

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- This is an example hint.
- This is an example hint.

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}

```

`@solution`
```{python}

```

`@sct`
```{python}
# Examples of good success messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.
```
