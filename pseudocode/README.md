<h1>
  <span class="headline">Fundamentals of Algorithms and Pseudocode</span>
  <span class="subhead">Pseudocode</span>
</h1>

**Learning objective:** By the end of this lesson, you will be able to express any algorithm using pseudocode

## An introduction to pseudocode
There are many ways of representing an algorithm. It may differ based on the audience whom it's intended for. For a non-technical audience with no programming language expertise, it can be represented visually in form of a **Flowchart**, or textually in form of **step-by-step instructions in plain English**. 

**Pseudocode** is a non-executable textual representation of an algorithm meant for a technical audience with even beginner-level programming knowledge or expertise in any programming language. It is a "text-based" design tool for programmers used in software development to design and communicate algorithms in a language-agnostic way. It provides a structured way to plan solutions without worrying about the syntax of a specific programming language.

#### Example:
Here's a pseudocode representation of the Amstrong number checking algorithm.
```plaintext
INPUT n 
SET cubeSum = 0 and temp = n.
REPEAT UNTIL (temp != 0)
  COMPUTE lastDigit = temp % 10
  COMPUTE cubeSum = cubeSum + (lastDigit * lastDigit * lastDigit)
  COMPUTE temp = temp / 10
IF (cubeSum == n)
  OUTPUT "Armstrong number"
ELSE
  OUTPUT "Not an Armstrong number"
```

### Benefits of pseudocode
1. Focuses on problem-solving rather than coding.
2. Acts as a blueprint for developers.
3. Facilitates effective communication between technical and non-technical stakeholders within a software development team.
4. Simplifies debugging and testing logical flows before implementation.

## Standards in pseudocode
There are no globally agreed standards available to write the pseudocode. Every organisation might use their own standards. However, there are some common syntax elements that are followed all over with organisation specific variations in vocabulary.

### Vocabulary - categories
- **Input action verbs** : `INPUT`, `GET`, `READ`, `OBTAIN`
- **Output action verbs** : `OUTPUT`, `PRINT`, `DISPLAY`, `SHOW`
- **Computational/processing action verbs** : `COMPUTE`, `CALCULATE`, `DETERMINE`
- **Flow control structure functions** : `IF`, `ELSE`, `ELSEIF`, `FOR`, `FOR EACH`, `DO WHILE`, `REPEAT UNTIL`, `CASE`
- **Data handling action verbs** : `SET`, `ASSIGN`, `INITIALIZE`, `INCREMENT`, `DECREMENT`
- **Subroutine functions** : `FUNCTION`, `PROCEDURE`, `CALL`, `RETURN`

### Syntax design principles as best practices
- **Be language agnostic** : Avoid implementing syntax elements specific to programming languages such as statement end markers, comment symbols, etc. Make the statement structure as close as possible to spoken english grammar.
- **Provide functional clarity** : Clearly categorise statements as input, processing or output statements. A single statement must not perform two categorically different functions.
- **Provide Structural clarity** : Use indentation to clearly show control structures, subroutines, and their nested hierarchies (if any). 
- **Keep it simple** : The pseudocode has only one responsibility - To make the algorithmic logic clear. It need not worry about solving additional technical considerations such as data types, memory management, 

