---
title: 'Chapter 5 - Iteration'
description: 'Chapter 5 Iteration learning objective here'
---

## While Loop Syntax

```yaml
type: PureMultipleChoiceExercise
key: 475c891694
xp: 50
```

<b><br><u>Syntax:</u><br>while *condition*:
     <br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Indented statement block to execute</b>

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

## Infinite Loop

```yaml
type: PureMultipleChoiceExercise
key: 5606092a39
xp: 50
```

A while loop can be used to repeat identical tasks until a specific condition is met. If a condition is not defined properly, this can cause infinite looping. Additional control features must be present to contain looping iterations.

>Which of the following <b>*will*</b> result in an infinite loop?

`@hint`
- n is a boolean
- This is an example hint.

`@possible_answers`
- n = True
<br>while n = 0:
<br>&nbsp;&nbsp;&nbsp;&nbsp; print("hello!")
- n = 3
<br>while n > 4:
<br>&nbsp;&nbsp;&nbsp;&nbsp; print("hello!")
- [n = 2
<br>while n == 2:
<br>&nbsp;&nbsp;&nbsp;&nbsp; print("hello!")]

`@feedback`
<!-- Examples of good feedback messages: https://instructor-support.datacamp.com/en/articles/2299773-exercise-success-messages.  -->
- Incorrect. The loop will never execute, n is a boolean and there is an error in the while condition syntax
- Incorrect. The loop will never execute because n = 3 which is always less than 4.
- Correct! Since n has no additional control features, this loop will indefinitely execute

---

## Copy of Infinite Loop

```yaml
type: PureMultipleChoiceExercise
key: 861aed773f
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

## use loop idioms

```yaml
type: BulletExercise
key: c1af8439fe
xp: 100
```

<!-- Guidelines for contexts: https://instructor-support.datacamp.com/en/articles/2375528-course-iterative-exercises -->

`@pre_exercise_code`
```{python}

```

---

## Use break

```yaml
type: NormalExercise
key: cb05bb01cb
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

---

## Use Continue

```yaml
type: NormalExercise
key: 2b3a1d5cdb
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
