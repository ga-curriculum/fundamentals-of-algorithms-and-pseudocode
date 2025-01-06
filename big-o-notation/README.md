<h1>
  <span class="headline">Fundamentals of Algorithms and Pseudocode</span>
  <span class="subhead">Big-O Notation</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to ascertain the efficiency of an algorithm using its Big-O notation.

## What is a good algorithm?
CPU time and memory space are limited resources on a computer shared by multiple programs. Even before a single line of code is written, algorithms can give insights into how much space and how much CPU time will be needed when they are eventually translated into actual computer programmes. The more CPU time and memory space a program consumes, the more complex it is said to be. 

### Time complexity
An algorithm's time complexity is the amount of time required to complete the execution. The time complexity is directly related to the number of algorithmic steps required to finish the execution. More the time complexity, more the number of CPU instructions and execution time.

### Space complexity
An algorithm's space complexity is the amount of memory units required by its data structures that are used during the algorithm's execution time. More the space complexity, the more memory space consumed by the program.

There can be multiple algorithms to solve a specific problem. However, a good algorithm is one that possesses the least time complexity and space complexity.

## The Big-O notation
Big-O notation is one of the most fundamental tools for computer scientists to analyze the time complexity of an algorithm. It is a mathematical notation used to describe the asymptotic growth in the number of steps of an algorithm (time complexity) as its input grows infinitely large.
It is expressed using the algebraic expression **O\(f\(n\)\)** where:
- "O" repreresents the phrase _Order of growth_.
- "n" represents the number of inputs.
- "f\(n\)" represents the order of growth of the time complexity of an algorithm in relation to it's number of inputs. 

In simple words, if we plot the number of data item inputs to an algorithm on x-axis and the number of executed steps for the algorithm on y-axis, then Big O notation represents the curve plotted for values from 0 to infinity on the x-axis. The steeper the curve climbs, the more the time complexity of the algorithm.


## The eight orders of growth

There are 8 possible algebraic orders of growth that can be represented by f\(n\).

### 1. O\(1\) - Constant time complexity
An algorithm is said to possess constant time complexity if the runtime is constant and does not depend on the size of the input.
#### **Pseudocode example**: Checking if the first element in an array is greater than a given number.
```plaintext
FUNCTION isFirstElementGreater(array, value):
    IF array[0] > value
        RETURN true
    ELSE
        RETURN false
```

### 2. O\(log n\) - Logarithmic time complexity
An algorithm is said to possess logarithmic time complexity if the runtime grows logarithmically, often when the problem size is divided in each iteration.
#### **Pseudocode example**: Counting the number of steps to repeatedly divide the array size by 2 until it reaches 1.
```plaintext
FUNCTION countSteps(array):
    SET steps = 0
    SET size = array.length

    WHILE size > 1:
        COMPUTE size = size / 2
        INCREMENT steps BY 1
    
    RETURN steps
```

### 3. O\(n\) - Linear time complexity
An algorithm is said to possess linear time complexity if the runtime grows proportionally with the input size.
#### **Pseudocode example**: Calculating the sum of all elements in an array.
```plaintext
FUNCTION calculateSum(array):
    SET sum = 0
    FOR i = 0 TO array.length - 1:
        COMPUTE sum = sum + array[i]
    
    RETURN sum
```

### 4. O\(n log n\) - linearithmic time complexity
An algorithm is said to possess linearithmic time complexity if the runtime grows faster than linear but slower than quadratic, often seen in divide-and-conquer approaches.
#### **Pseudocode example**: A recursive algorithm that splits the array into two halves and performs linear operations on each half.
```plaintext
FUNCTION processArray(array):
    IF array.length == 1:
        RETURN performLinearOperation(array)  # Base case

    COMPUTE mid = array.length / 2
    SET left = array[0:mid]
    SET right = array[mid:end]

    CALL processArray(left)
    CALL processArray(right)

    RETURN combineResults(left, right)
```

### 5. O\(n^2\) - Quadratic time complexity
An algorithm is said to possess quadratic time complexity if the runtime grows quadratically with the input size, typically due to nested loops.
#### **Pseudocode example**: Comparing every pair of elements to find duplicates.
```plaintext
FUNCTION findDuplicates(array):
    FOR i = 0 to array.length - 1:
        FOR j = i + 1 TO array.length - 1:
            IF array[i] == array[j]:
                PRINT ("Duplicate found:", array[i])
```

### 6. O\(n^3\) - Cubic time complexity
An algorithm is said to possess cubic time complexity if the runtime grows cubically, often due to three nested loops.
#### **Pseudocode example**: Calculating the sum of all possible triplets of elements in the array.
```plaintext
FUNCTION calculateTripletSum(array):
    SET sum = 0
    FOR i = 0 TO array.length - 1:
        FOR j = i + 1 TO array.length - 1:
            FOR k = j + 1 TO array.length - 1:
                COMPUTE sum = sum + (array[i] + array[j] + array[k])

    RETURN sum
```

### 7. O\(2^n\) - Exponential time complexity
An algorithm is said to possess exponential time complexity if the runtime doubles with each additional input, typically seen in recursive algorithms that solve all subsets of the input.
#### **Pseudocode example**: Generating all subsets of an array.
```plaintext
FUNCTION generateSubsets(array, index = 0, current = []):
    IF index == array.length:
        PRINT (current)
        RETURN

    # Exclude current element
    CALL generateSubsets(array, index + 1, current)

    # Include current element
    CALL generateSubsets(array, index + 1, current + [array[index]])
```

### 8. O\(n!\) - Factorial time complexity
An algorithm is said to possess factorial time complexity if the runtime grows factorially, usually seen in algorithms that generate all permutations.
#### **Pseudocode example**: Generating all permutations of an array.
```plaintext
FUNCTION generatePermutations(array, current = []):
    IF array is empty:
        PRINT (current)
        RETURN

    FOR i = 0 TO array.length - 1:
        COMPUTE remaining = array[0:i] + array[i+1:end]
        CALL generatePermutations(remaining, current + [array[i]])
```

## Ascertaining an algorithm's Big-O
### Step 1: Identify the dominant terms
We have to examine the algorithm and identify the input data items that cause the maximum number of repetitive statement executions. These input data items are called the dominant terms. In our analysis, we should consider the input data items directly or indirectly used by looping control structures and nested loops.

### Step 2: Determine the order of growth f(n)
Now we have to numerically calculate the increase in the number of executed statements of the algorithm for one increment of dominant term(s). This can be repeated for 3 increments to express the relationship in form of an algebraic expression.

#### For example, lets say:
- When input count of dominant term n = 1, the respective number of executed algorithmic statements f\(n\) is 20.
- When input count of dominant term n = 2, the respective number of executed algorithmic statements f\(n\) is 30.
- When input count of dominant term n = 3, the respective number of executed algorithmic statements f\(n\) is 40.

This relationship can be expression
```plaintext
f(n) = 10n + 10
```
### Step 3: Express the order of growth in Big-O notation
The Big-O notation is expressed as `O(f(n))`. For our example, it will be `O(10n+10)`.

We know that Big-O notation is not used to express the accurate numerical growth of number of executed statements, but to express only the order of growth. Hence, our Big-O notation can be further simplified by removing the constants and multipliers in the equation as they do not contribute to the order of the algebraic equation.

Upon simplifying `O(10n+10)` by removing constants and multipliers, we arrive at our final Big-O notation `O(n)`. This means our algorithm's time complexity is linear.



## Closing reflections
The lesser the time complexity of an algorithm, the better its performance will be when converted to code. Here is a table of Big-O notations arranged from least complex to most complex:

|**Big O Notation**|**Growth nature**|
|:---|:---|
|O(1) - Constant time complexity|Constant. The least complex algorithms.|
|O(log n) - Logarithmic time complexity|Grows slowly.|
|O(n) - Linear time complexity|Grows proportionally.|
|O(n log n) - Linearithmic time complexity|Grows faster than linear.|
|O(n^2) - Quadratic time complexity|Grows quadratically(squared).|
|O(n^3) - Cubic time complexity|Grows cubically.|
|O(2^n) - Exponential time complexity|Grows exponentially.|
|O(n!) - Factorial time complexity|Grows factorially. The most complex algorithms.|
