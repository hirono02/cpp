# Arithmetic Operators in C++
- Arithmetic operators are used to perform mathematical operations with basic variables such as integers and floating-point numbers

### Addition Operator
- It adds 2 numbers together    
`int sum = a + b;`

### Subtraction Operator
- It subtracts one number from another    
`int difference = a - b;`  

### Multiplication Operator
- It multiplies two numbers together    
`int product = a * b;`  

### Division Operator
- It divides one number by another
- If both operands are integers, it will perform integer division and the result will be an integer
`int quotient = a / b;` -> Integer division   
`float quotient = float (a) / float (b);` -> Floating-point division   

### Modulus Operator
- It calculates the remainder of an integer division  
`int remainder = a % b;`

### Increment Operator
- It increments the value of a variable by 1     
- There are 2 ways to use this operator 
    - prefix (`++x`): This increments the value before returning it
    - postfix (`x++`): This returns the value first and then increments it
```
int x = 5;     
int y = ++x;    // x = 6, y = 6   
int z = x++;    // x = 7, z = 6
```

### Decrement Operator
- It decrements the value of a variable by 1
- It can also be used in prefix and postfix forms
```
int x = 5;
int y = --x;    // x = 4, y = 4
int z = x--;    // x = 3, z = 4
```
