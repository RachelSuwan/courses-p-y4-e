---
title: 'Chapter 5 - Iteration'
description: 'Chapter 5 Iteration learning objective here'
---

## Indefinite and Infinite Loop

```yaml
type: PureMultipleChoiceExercise
key: 5606092a39
xp: 50
```

While loops will run until a condition is met. While Loop implementation may make it an indefinite loop because the number of iterations the loop is to run is unknown prior to running, not set, or not easily computed. 
<b><br><u>Syntax:</u><br>while *condition*:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute</b>
     <br>
     <br>A while loop can be used to repeat identical tasks until a specific condition is met. If a condition is not defined properly, this can cause infinite looping. Additional control features must be present to contain looping iterations. An example of an additional control is an iteration variable, which gets updated with every loop execution.

>Which of the following <b>*will not*</b> result in an infinite loop?

`@hint`
-
-

`@possible_answers`
- n = 5
<br>while True:
<br>&nbsp;&nbsp;&nbsp;&nbsp; print("hello!")
- n = 5
<br>while n > 4:
<br>&nbsp;&nbsp;&nbsp;&nbsp; print("hello!")
<br>&nbsp;&nbsp;&nbsp;&nbsp; n++
- [] n = 0
<br>while n < 2:
<br>&nbsp;&nbsp;&nbsp;&nbsp; print("hello!")
<br>&nbsp;&nbsp;&nbsp;&nbsp; n++ ]

`@feedback`
<!-- Examples of good feedback messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.  -->
- Incorrect.
- Incorrect. While the iteration variable is updated in the loop, since it starts at 5 it will always execute. It would be a valid control feature if n--
- Correct!

---

## Using Continue and Break

```yaml
type: DragAndDropExercise
key: 1d67e6739e
kind: Parsons
xp: 100
```

To add flexibility to `while` loops, keywords like `continue` and `break` can be utilized.
<br>
<br> `continue` offers the ability to skip the remainder of the loop it is called in, for the *current* iteration. 
<br>
<br> `break` allows a complete exit from the loop.

`@instructions`
This code should print the numbers 1 to 5. Rearrange the code to reflect the following order (*make sure to indent where necessary*):
- If n equals 5, skip the iteration
- If n equals 6, exit the loop
- Increment variable
- Print the increment variable value

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- By using the `< >` on the right side of the elements, you can adjust the required indentation
- `n = 0` and `while True:` should have no indentations
- `if n == 5:`, `if n == 6:`, `n = n + 1`, `print(n)` should have 1 indentation apiece
- `continue` and `break` should have 2 indentations apiece

`@solution`
```{python}
- id: a
  title: Program
  language: python
  maxOffset: 2 #determines the indents
  items:
    - content: 'n = 0'
      id: id_0
    - content: 'while True:'
      id: id_1
    - content: 'if n == 5'
      id: id_2
      offset: 1
    - content: 'continue'
      id: id_3
      offset: 2
    - content: 'if n == 6'
      id: id_4
      offset: 1
    - content: 'break'
      id: id_5
      offset: 2
    - content: 'n = n + 1'
      id: id_6
      offset: 1
    - content: 'print(n)'
      id: id_7
      offset: 1
```

`@sct`
```{python}
checks:
  - condition: check_index(id_0) == solution
    incorrectMessage: "Start by defining the increment variable" # If that condition is not true, show this message.
  - condition: check_index(id_1) == solution
    incorrectMessage: "Define the loop after defining the increment variable"
  - condition: check_index(id_2) == solution
    incorrectMessage: "As per the instructions, if n == 5: must come before n == 6:"
  - condition: check_index(id_3) == solution
    incorrectMessage: "continue belongs in the if statement with the condition n == 5"
  - condition: check_index(id_4) == solution
    incorrectMessage: "As per the instructions, if n == 6: must come after n == 5:"
  - condition: check_index(id_5) == solution
    incorrectMessage: "break belongs in the if statement with the condition n == 6"
  - condition: check_index(id_6) == solution
    incorrectMessage: "Increment variable after break and continue statements"
  - condition: check_index(id_7) == solution
    incorrectMessage: "Lastly, print the increment value"
 
successMessage: 'Well done!' # Message shown when all is correct.
errorMessage: 'Try again, you can do it!' # Message shown when there are errors (and there is no specific error available).
isOrdered: true  # Should the items in the zones be ordered as in the solution code?
```

---

## Definite Loops

```yaml
type: NormalExercise
key: 2b3a1d5cdb
xp: 100
```

Definite loops have a known number of iterations defined prior to entering the loop. An example of a definite loop would be the `for` statement. 
<b><br><u>Syntax:</u><br>for *variable* in *set*:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute</b>
     <br>

`@instructions`
Frank wants to say hello to each person in his family. 
- for each `person` in family print "Hello", person!

`@hint`
<!-- Examples of good hints: https://instructor-support.datacamp.com/en/articles/2379164-hints-best-practices. -->
- Follow the syntax listed in context above
- your code should look like -- `for person in family:`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
family = ['Mom', 'Dad', 'Sister', 'Brother']

```

`@solution`
```{python}
for person in family:
    print("hello",person)
```

`@sct`
```{python}
Ex().check_for_loop().multi(
    check.iter().has_equal_value(),
    check.body().has_equal_output() 
    )
success_msg("Great Job!")
```

---

## Parsons Drag and Drop, syntax 

```yaml
type: DragAndDropExercise
key: c5cbff1d76
kind: Parsons
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

`@solution`
```{python}
# Edit or remove this code to create your own exercise.
# This is 1 type of drag and drop exercise, there are 2 other types. See documentation:
# http://instructor-support.datacamp.com/en/articles/3039539-course-drag-drop-exercises

# Make sure you only use SPACES, NOT TABS in front of each line.
- id: a
  title: Program
  language: python
  maxOffset: 2
  items:
    - content: 'def is_true(boolean_value):'
      id: id_0
    - content: 'if boolean_value:'
      id: id_1
      offset: 1
    - content: 'return True'
      id: id_2
      offset: 2
    - content: 'return False'
      id: id_3
      offset: 1
```

`@sct`
```{python}
checks:
  - condition: check_index(id_0) == solution
    incorrectMessage: "Start by defining the function" # If that condition is not true, show this message.
  - condition: check_index(id_1) == solution
    incorrectMessage: "Start with a check on the function argument"
  - condition: check_index(id_2) == solution
    incorrectMessage: "Try again, you can do it!"
  - condition: check_index(id_3) == solution
    incorrectMessage: "We believe in you, try again!"
successMessage: 'Well done!' # Message shown when all is correct.
errorMessage: 'Try again, you can do it!' # Message shown when there are errors (and there is no specific error available).
isOrdered: true  # Should the items in the zones be ordered as in the solution code?
```

---

## Use definite loop

```yaml
type: NormalExercise
key: b1d008b67d
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
