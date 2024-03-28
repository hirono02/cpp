# Static Typing
In C++, static typing means that the data type of a variable is deteremind at compile time, before the program is executed. This means that a variable can be used only with the data of a specific type, and the compiler ensures that the operations performed with the variable are compatible with its type.

C++ uses static typing to determine data types and perform type checking during **compile time**. This helps with ensuring type safeety and can prevent certain types of errors from occurring during the execution of the program.  

Example:   
```
#include <iostream>

int main() {
    int num = 42;           // 'num' is statically typed as an integer
    double pi = 3.14159     // 'pi' is statically typed as a double

    num = pi;    // this would cause a compile-time error as the types don't match
    return 0;
}
```

In th code above, the variable `num` is statically typed as an `int` and `pi` is statically typed as a `double`. If we attempted to assign the value of `pi` to `num`, we would get a compile-time error. This is because the system ensures that variables are only used with compatible data types.