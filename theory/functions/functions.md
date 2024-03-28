# Functions in C++
A **function** is a group of statements that perform a specific task, organized as a separate unit in a program. Functions help in breaking the code into smaller, manageable, and reusable blocks   

There are mainly 2 types of functions in C++:
- **Standard library functions**:
    - These are pre-defined functions available in the C++ standard library, such as `printf()`, `scanf()`, `sqrt()`, and many more
    - These functions are part of the standard library, so we need to include the appropriate header file to use them.
- **User-defined functions**: 
    - These are functions created by the programmer to perform a specific task
    - In order to create a user-defined funciton, we need to define the function and call it in the code

### Defining a function
- The general format for defining a function in C++ is:
```
return_type function_name(parameter list) {
    // function body
}
```
- `return_type`: Data type of the output produced by the function. It can be `void`, indicating that the function doesn't return any value
- `function_name`: Name given to the function, following C++ naming conventions
- `parameter list`: List of input paraneters/arguments that are need to perform the task. It is optional, and when no parameters are needed, we can leave it blank or use the keyword `void`.

Example:   
```
#include <iostream>

// Functions to add 2 numbers
int addNumbers(int a, int b) {
    int sum = a + b;
    return sum;
}

int main() {
    int num1 = 5, num2 = 10;
    int result = addNumbers(num1, num2);    // calling the function
    std::cout << "The sum is: " << result << std::endl;
    return 0;
}
```
In this example, the function `addNumbers` takes 2 integer parameters, `a` and `b`. It then returns and displays the sum of the numbers after being called from the `main()` function


### Function Prototypes
In some cases, we might want to use a function before actually defining it   
In order to do this, we need to declare a **function prototype** at the beginning of our code.  
   
A function prototype is a declaration of the function without its body, and it informs the compiler about the function's name, return type, and parameters.
```
#include <iostream>

// Function prototype
int multiplyNumbers(int x, int y);

int main() {
    int num1 = 3, num2 = 7;
    int result = multiplyNumbers(num1, num2);   // Calling the function
    std::cout << "The product is: "<< result << std::endl;
    return 0;
}

// Function definition
int multiplyNumbers(int x, int y) {
    int product = x * y;
    return product;
}
```