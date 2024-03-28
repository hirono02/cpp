# Data Types in C++
Data types are used to categorize different types of data that a program can process.   
They are essential for determining the type of value a variable can hold and how much memory space it will occupy. Some basic data types in C++ include integers, floating-point numbers, characters, and booleans.

## Fundamental Data Types
### Integer (int)
Integers are whole numbers that can store both positive and negative values. The size of `int` depends on the system architecture (usually 4 bytes).   

Example:  
`int num = 42;`

There are variants of `int` that can hold different ranges of numbers:
- short (`short int`): Smaller range than `int`
- long (`long int`): Larger range than `int`
- long long (`long long int`): Even larger range than `long int`

### Floating-point (float, double)
Floating point types represent real numbers, i.e., numbers with a decimal point.
There are 2 main floating-point types:
- **float**: Provides single-precision floating-point numbers. It typically occupies 4 bytes of memory  
  
Example:    
`float pi = 3.14f;`
- **double**: Provides double-precision floating-point numbers. It consumes more memory (usually 8 bytes) but has a higher precision than `float`  

Example:   
`double pi_high_precision = 3.1415926535;`

### Character (char)
Characters represent a single character, such as a letter, digit, or symbol. They are stored using the  ASCII value of the symbol and typically occupy 1 byte of memory   

Example:   
`char letter = 'A';`

### Boolean (bool)
Booleans represent logical values: `true` or `false`. They usually occupy 1 byte of memory  

Example:  
`bool is_cpp_great true;`



