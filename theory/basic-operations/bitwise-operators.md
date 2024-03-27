# Bitwise Operations
- Bitwise operations are operatrions tha directly manipulate the bits of a number
- This operation is useful for various purposes, such as:
    1. Optimizing algorithms
    2. Performing certain calculations
    3. Manipulating memory in lower-level programming languages like C and C++

### Bitwise AND (&)
- The bitwise AND operation (`&`) is a binary operation that takes 2 numbers, compares them bit by bit, and returns a new number where each bit is set (1) if the corresponding bits in both input are set (1). Otherwise, the bit is unset (0)   

Example:    
```
int result = 5 & 3; // result will be 1 (0000 0101 & 0000 0011 = 0000 0001)
```

### Bitwise OR (|)
- The bitwise OR operation (`|`) is a binary operation that takes 2 numbers, compares them bit by bit, and returns a new number where each bit iss set (1) if at least one of the corresponding bits in either input number is set (1). Otherwise, the bit is unset (0)    

Example:
```
int result = 5 | 3; // result will be 7 (0000 0101 | 0000 0011 = 0000 0111)
```
