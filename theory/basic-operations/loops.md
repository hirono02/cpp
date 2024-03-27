# Loops in C++
- Loops are an essential programming concept that allows us to repeatedly execute a block of code until a specific condition is met.
- In C++, there are 3 main types of loops: `for`, `while`, and `do-while`

### For Loop
- A `for` loop is used when we know the number of times we want to traverse through a block of code
- It consists of an initialization statement, a condition, and an increment/decrement operation
- This is the syntax for a `for` loop:   
```
for (initialization; condition; increment/decrement) {
    /// block of code to execute
}
```    

For example:   
```
#include <iostream>

int main() {
    for (int i = 0; i < 5; i++) {
        std::cout << "Iteration: " << i << std::endl;
    }
    return 0;
}
```
