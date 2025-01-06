<h1>
  <span class="headline">Fundamentals of Algorithms and Pseudocode</span>
  <span class="subhead">Algorithms</span>
</h1>

**Learning objective:** By the end of this lesson, you'll be able to explain what an algorithm is.

## Problem solving using data and logic
The 1880 census of United States of America took 8 years to process the collected data and publish the statistics. This delayed a lot of public policy and tax decisions which relied on the census data. When it was time for 1890 census, the US government turned towards a German-American statistician and inventor named Hermann Hollerith to improve the efficiency processing census data.
Exclusively for the purpose of the 1890 census, Hermann Hollerith invented three things. 
1. A **Punch Card** with a matrix of 12 rows and 20 columns to record the census data in form of hole punches. For example, a specific cell of the matrix might represent a census data item like marital status. A hole in that cell meant married and no hole meant unmarried. 
2. A mechanical **Key Punch** machine using which a human operator can code the answers to 30 census questions on a family census card into a matrix of holes and no-holes on the punch card. 
3. An electro-mechanical **Tabulator** machine, which can read the punch card and its mechanics would move the needles on 52 accumulator dials. Each dial was counting a particular census statistic and it's count increased by based on holes in one or more cells.

These inventions reduced the time taken to process and publish the 1890 census data in 3 months. This marked the dawn of computing age where complex problems can be solved with high accuracy and less time by machines that can:
- Structure the problem-related data in a way that takes less space to store and easy to access by a computing machine.
- Perform computational logic on structured data to solve the problems in least amount of time.  


## Algorithms
An algorithm is a descriptive logic of a solution to a problem. It is not the program or code. Just logic.
Formally, an algorithm is defined as a finite set of instructions which are being carried in a specific order to perform the specific task. 

Such a descriptive algorithm must have three features: 
- **Definiteness** - No step in an algorithm can have multiple interpretations
- **Finiteness** - An algorithm must possess a finite number of steps
- **Effectiveness** - An algorithm must solve a problem by producing the necessary output(s) using a finite number of inputs.

#### Example:
Here's an example of an algorithm to find whether a number is Amstrong number or not. An Armstrong number is a number that is equal to the sum of cubes of its digits. For example, 153 is an Armstrong number because (1^3)+ (5^3)+(3^3) = 153.
```plaintext
Step 1: Initialize variable n to a random test number to check if it is Armstrong number.
Step 2: Initialize variable cubeSum to 0.
Step 3: Initialize variable temp to n.
Step 4: Repeat below steps while the value of n stays greater than zero.
  Step 4.1: Find the reminder when n is divided by 10 and store it in variable 'lastDigit'.
  Step 4.2: Remove the last digit from n by dividing its current value by 10 and storing the quotient in n iteself.
  Step 4.3: Add the cubed value of lastDigit to cubeSum and store it in cubeSum.
Step 5: If temp == cubeSum then Print "Armstrong number"
STep 6: Else Print "Not an Armstrong number"
``` 

## Data structures
A data structure is the structure in which multiple data items, that are related to a problem, are stored and organized in the computer's physical memory space. Data structures may vary depending on the algorithm using the least amount of steps. Data structures are classified into two categories:

### 1. Linear data structures
A linear data structure is one in which the data items are stored sequentially, and the data items are connected to the previous and the next element. As the data items are stored sequentially, so they can be traversed or accessed in a single run. The implementation of linear data structures is easier as the data items are sequentially organized in memory. Arrays are an example of linear data structures.

### 2. Non-linear data structures
A non-linear data structure one in which the data data items are not arranged in a contiguous manner. As the arrangement is non-sequential, so the data data items cannot be traversed or accessed in a single run. In the case of linear data structure, element is connected to two data items (previous and the next element), whereas, in the non-linear data structure, an element can be connected to more than two data items. Trees are an example of non-linear data structures.

## Fundamental algorithms
The fundamental algorithms that work on data structures are:
- **Search algorithms**: Step-by-step instructions for searching and finding a specific data item inside a data structure.

- **Sort algorithms**: Step-by-step instructions for sorting the data items in a certain order. They prepare the data structure for search algorithms. Search algorithms need less instructions, and hence, work faster on a sorted data structure as opposed to an unsorted data structure.

Search and sort algorithms form the basis on which complex algorithms can be built. Once the data item needed by the algorithm is located within a data structure, in the subsequent steps, that data item can be read and used for further computations, replaced, or removed.

