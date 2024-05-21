# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Fundamentals of Algorithms and Pseudocode

| Title                                     | Type    | Duration | Author               |
|-------------------------------------------|---------|----------|----------------------|
| Fundamentals of Algorithms and Pseudocode | Lecture | 1:00     | Suresh Melvin Sigera |

## Introduction

Welcome to "Fundamentals of Algorithms and Pseudocode" In this lesson, we will explore the foundational concepts of
algorithms and pseudocode, essential tools for any aspiring programmer. Algorithms are step-by-step procedures for
solving problems and performing tasks, which we'll learn to express through pseudocode—a simplified, language-agnostic
way of outlining an algorithm's logic.

## Learning Objectives

By the end of this lesson, you will be able to:

1. Understand the basic structure and purpose of algorithms.
2. Write and interpret pseudocode.
3. Identify and use key pseudocode terminology and syntax rules.
4. Apply algorithms to solve simple problems using pseudocode.

## Lesson Overview (60 Min)

1. [What is an Algorithm?](#What-is-an-Algorithm)
4. [Keywords and Commands](INSERTURL)
5. [Common Structures in Pseudocode](#Common-Structures-in-Pseudocode)
6. [Exercise](#Exercise-Debugging-a-Peanut-Butter-and-Jelly-Sandwich-Algorithm)
7. [Summary and Key Takeaways](#Summary-and-Key-Takeaways)

## What is an Algorithm?

An algorithm is a `procedure` for solving a problem in terms of the actions to be executed, and the order in which those
actions are to be executed. An algorithm is merely the sequence of steps taken to solve a problem. The steps are
normally "sequence," "selection, " "iteration," and a case-type statement.

### Introduction to Pseudocode

Pseudocode is an artificial and informal language that helps programmers develop algorithms. It is a "text-based" design
tool that uses simple language to express complex instructions.

### Syntax and Rules of Pseudocode

The rules of Pseudocode are reasonably straightforward. All statements showing "dependency" are to be indented. These
include while, do, for, if, switch. Examples below will illustrate this notion.

Examples:

```text
If student's grade is greater than or equal to 60
    Print "passed"
else
    Print "failed"
endif
```

```text
Set total to zero
Set grade counter to one
while grade counter is less than or equal to ten
    Input the next grade
    Add the grade into the total
endwhile
Set the class average to the total divided by ten
Print the class average.
```

```text
Initialize total to zero
Initialize counter to zero
Input the first grade
while the user has not as yet entered the sentinel
    add this grade into the running total
    add one to the grade counter
    input the next grade (possibly the sentinel)
endwhile
if the counter is not equal to zero
    set the average to the total divided by the counter
    print the average
else
    print 'no grades were entered'
endif
```

```text
initialize passes to zero
initialize failures to zero
initialize student to one
while student counter is less than or equal to ten
    input the next exam result
    if the student passed
        add one to passes
    else
        add one to failures
    endif
endwhile
add one to student counter
print the number of passes
print the number of failures
if eight or more students passed
    print "raise tuition"
endif
```

### Keywords and Commands

The keywords that are to be used
include `Do While`...`EndDo`; `Do Until`...`Enddo`; `Case`...`EndCase`; `If`...`Endif`; `Call`...
with `(parameters)`; `Call`; `Return` ....; `Return`; `When`; Always use scope terminators for loops and iteration.

As verbs, use the words `Generate`, `Compute`, `Process`, etc. Words such
as `set`, `reset`, `increment`, `compute`, `calculate`, `add`, `sum`, `multiply`, ... `print`, `display`, `input`, `output`, `edit`, `test` ,
etc. with careful indentation tend to foster desirable pseudocode.

NOTE : Do not include data declarations in your pseudocode.

### Pseudocode standard

Common categories of actions include:

- Input: `GET`, `READ`, `OBTAIN`
- Output: `PRINT`, `DISPLAY`, `SHOW`
- Compute: `COMPUTE`, `CALCULATE`, `DETERMINE`
- Initialize: `SET`, `INIT`
- Add One: `INCREMENT`, `BUMP`
- Function: `PROCEDURE`

## Common Structures in Pseudocode

Examples of structures include Sequence, If-Then-Else, While, Case, Repeat, and For loops. Sequence: A series of
instructions (list of actions) at the same level of indentation. Means complete one action and proceed to the next

### Examples of Pseudocode

Here we illustrate the use of pseudocode with simple algorithm examples like calculating class averages, determining if
a number is odd or even, and more.

Example:

```text
GET temperature value
GET weather type
PRINT “It is <temperature> degrees and <weather type> out right now”
``` 

### If-Then-Else:

A decision between two sequences based on some condition (NOTE: the indentation of the then and else sequences)

```text
GET num
IF num % 2 THEN
  PRINT “<num> is even!”
ELSE
  PRINT “<num> is odd!”
ENDIF
```

### While:

As long as some condition is met, continuously run the same sequence (NOTE: once again we have the body of the while
loop indented)

```text
DETERMINE buellerIsPresent
WHILE !buellerIsPresent
  PRINT “Bueller? …”
  DETERMINE buellerIsPresent
ENDWHILE
```

### Case:

Like an if-else statement but matching on a particular value (NOTE: if we want our case statement to be comprehensive,
we need to provide a default case under OTHER)

```text
CASE temp OF:
  “Cold”: PRINT “Better stay indoors...”
  “Cool”: PRINT “Bring a jacket!”
  “Warm”: PRINT “Enjoy the sun!”
  OTHERS:
    PRINT: “Unknown temp! You’re on your own!”
ENDCASE
```

### Repeat:

```text
REPEAT:
  PRINT “Pete and Repete were sitting on a bridge. Pete fell off. Who was left?”
  GET userAnswer
UNTIL userAnswer != ‘Repete’
```

### For:

A for loop is just a specialized while loop that loops over elements of some collection

```text
GET limit
FOR each number up to limit
  IF number is divisible by 5 and 3 THEN
     PRINT “FizzBuzz”
  ELSE IF number is divisible by 3 THEN
    PRINT “Fizz”
  ELSE IF number is divisible by 5 THEN
    PRINT “Buzz”
  ELSE
    PRINT number
  ENDIF
ENDFOR
```

## Exercise: Debugging a Peanut Butter and Jelly Sandwich Algorithm

**Objective:** To understand the importance of precise instructions in programming and practice debugging skills.

**Task:** Write a pseudocode algorithm for making a peanut butter and jelly sandwich. Imagine you are instructing a
computer, which takes your instructions literally.

### Instructions:

1. **Watch the Video**: Before you start writing your pseudocode, watch this video
   on [How to make a peanut butter and jelly sandwich](https://www.youtube.com/watch?v=Ct-lOOUqmyY). Pay close attention
   to each step involved in the process.

2. **Initial Algorithm**: Write your first version of the pseudocode to make a peanut butter and jelly sandwich. List
   each step clearly and in order.

3. **Peer Review**: Swap your pseudocode with a partner and execute each other's instructions exactly as written. Note
   any ambiguities or missing steps where assumptions might be made.

4. **Identify Bugs**: List any issues or "bugs" that arose when your partner followed your pseudocode. Were there any
   steps that the computer (in this case, your partner) couldn't execute due to vague instructions?

5. **Revise Algorithm**: Using the feedback, revise your pseudocode to address the bugs. Be as specific and detailed as
   possible.

6. **Final Presentation**: Present your original and revised pseudocode. Explain the changes you made and why they were
   necessary to make the instructions clearer for the computer.

### Reflection:

Reflect on the challenges you faced when writing the pseudocode. Discuss how this exercise might relate to real-world
programming and the importance of debugging and precise communication in code development.

## Summary and Key Takeaways

In this lesson, we've explored the fundamental concept that computers operate strictly based on the commands they are
given—they do not have the ability to interpret or infer intent like humans do. This understanding is crucial for
writing effective algorithms and pseudocode, as it emphasizes the need for precision in programming.

**Key Takeaways:**

1. **Pseudocode Proficiency**: Students learn to use pseudocode effectively, enhancing their ability to plan and
   communicate algorithms clearly, which lays a strong foundation for understanding various programming languages.

2. **Debugging and Problem-Solving Skills**: Through practical exercises, such as debugging a simple pseudocode for
   making a sandwich, students develop essential debugging skills and a systematic approach to problem-solving that
   emphasizes logical thinking and precision.

3. **Creative and Logical Thinking**: The lesson encourages both creative and logical thinking by allowing students to
   explore multiple solutions to problems and demonstrating the importance of structured algorithm design in
   programming.

Remember, the clarity of your instructions directly impacts the effectiveness of the computer programs you create.