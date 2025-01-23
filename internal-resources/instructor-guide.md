<h1>
  <span class="headline">Fundamentals of Algorithms and Pseudocode</span>
  <span class="subhead">Instructor Guide</span>
</h1>

## Solution to independent practice 
### **Algorithm pseudocode**
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
### **Time Complexity**
The time complexity measures the number of steps or operations relative to the input size `n`.

1. **Loop Behavior**:
   - The loop (`REPEAT UNTIL temp != 0`) iterates once for each digit in the input `n`.
   - If `n` has `d` digits, the loop executes **d times**.
   - The number of digits in `n` can be expressed as `O(log₁₀(n))` in terms of `n`.

2. **Operations Inside the Loop**:
   - **Modulo Operation**: `temp % 10` takes constant time **O(1)**.
   - **Cube Calculation**: `(lastDigit * lastDigit * lastDigit)` is also constant-time **O(1)**.
   - **Division Operation**: `temp / 10` takes constant time **O(1)**.

   All operations within each loop iteration are **O(1)**.

3. **Overall Complexity**:
   - Since the loop runs **O(log₁₀(n))** times and the operations inside are **O(1)**, the total time complexity is O(log(n)).

### **Space Complexity**
The space complexity measures the amount of memory the algorithm uses relative to the input size.

1. **Auxiliary Variables**:
   - The algorithm uses a constant amount of space to store variables: `cubeSum`, `temp`, `lastDigit`, and `n`.
   - No additional memory is allocated dynamically (like arrays, stacks).

2. **Overall Complexity**:
   - The algorithm's space usage is constant and does not depend on the input size, so the space complexity is O(1)


### **Summary**
- **Time Complexity**:  O(log(n)), where `n` is the input number.
- **Space Complexity**: O(1), as the algorithm uses only a fixed amount of memory.