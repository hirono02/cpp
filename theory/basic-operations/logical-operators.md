# Logical Operators in C++
- Logical operators are used to perform logical operations on the given expressions, mostly to test the relationship between different variables or values
- They return a boolean value i.e, either true (1) or false (0) based on the result of the evaluation

C++ provides the following logical operators:
- AND Operator (&&)
    - This operator checks if both the operands/conditions are true, then the expression is true
    - Should any one of the condition be false, the whole expression will result to false     
    `(expression1 && expression2)`    
    
    Example:
    ```
    int a = 5, b = 10;
    if (a > 0 && b > 0) {
        std::cout << "Both values are positive." << std::endl; 
    }
    ```
- OR Operator (||)
    - This operator checks if either of the operands/conditions are true, and then the expression is true
    - If both the conditions are false, only then will it be false   
    `(expression1 || expression2)`  

    Example:
    ```
    int a = 5, b = -10;
    if (a > 0 || b > 0) {
        std::cout << "At least one value is positive." << std::endl;
    }
    ```