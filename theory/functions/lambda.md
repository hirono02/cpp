# Lambda Functions in C++
- A lambda function is an anonymous function that is defined in place, within the source code, and with a concise syntax
- Lambda functions were introduced in C++11 and have become a widely used feature, especially in combination with the Standard Library algorithms

### Syntax
- The example below is a basic syntax of a lambda function in C++    
```
[capture-list](parameters) -> return_type {
    // function body
};
```    
- **capture-list**: A list of variables from the surrounding scope that the lambda function can access
- **parameters**: The list of input parameters, just like in a regular function *(Optional)*
- **return_type**: The type of the value that the lambda function will return 
    - This part is optional, and in many cases can be deduced by the compiler
- **function body**: The code that defines the operation of the lambda function

### Usage Examples
These are a few examples to demonstrate the use of llambda functions in C++:
- Lambda function with no capture, parameters, or return type   
```
auto printHello = []() {
    std::cout << "Hello, World!" << std::endl;
};
printHello();   // Output: Hello, World!
```
- Lambda function with parameters
```
auto add = [](int a, int b) {
    return a + b;
}
int result = add(3, 4); // result = 7
```
- Lambda function with capture-by-value
```
int multiplier = 3;
auto times = [multiplier](int a) {
    return a * muiltiplier;
}
int result = times(5);  // result = 15
```
- Lambda function with capture-by-reference
```
int expiresInDays = 45;
auot updateDays = [&expiresInDays](int newDays) {
    expiresInDays = newDays;
}
updateDays(30); // expiresInDays = 30
```

Important to take not that when using the capture by reference, any change made to the captured variable inside the lambda function will affect its value in the surrounding scope
