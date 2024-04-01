# Memory Model in C++
The memory model in C++ defines how the program stores and accesses data in commputer memory. It consists of different segments, such as the Stack, Heap, Data, and Code segments. Each of these segments is used to store different types of data and has specific characteristics

### Stack Memory
Stack memory is used for *automatic storage duration variables*, such as local variables and function call data. Stack memory is managed by the **compiler**, and it's allocation and deallocation are done automatically.  

The stack memory is a LIFO (Last In First Out) data structure, meaning that the most recent data allocated is the first to be deallocated.  
```
void functionExample() {
    int x = 10; // x is stored in the stack memory
}  
```

### Heap Memory
Heap memory is used for *dynamic storage duration variables*, such as objects created using the `new` keyword. The programmer has control over the allocation and deallcation of heap memory using `new` and `delete` operators. Heap memory is a larger pool of memory than the stack, but has a slower access time.   

The slower access time can be attributed to several factors:
1. **Memory Allocation Mechanisms**: 
    - Stack memory is managed in a very organized way by the systemm, with memory being allocated and deallocated in a LIFO sequence. This makes stack oeprations very fast.
    - Heap memory is dynamically allocated and deallocated at runtime, which can lead to framentation and the need for more complex management algorihtms, slowing down access times.
2. **Locality of Reference**: 
    - Stack memory often beneifts from better locality of reference. Variables used in functions (which are stored on the stack), are likely to be accessed frequently over a short period of time, making it possible for those variables to be effectively cached by the CP
    - Heap memory is used for objects that might be accessed irrgularly, reducing the efficiency of CPU caching and thus increasing access times.
3. **Memory Caching**:
    - The stack's sequential nature of allocation and deallocation patterns makes it more predictable for caching mechanisms. Modern CPUs are optimized to take advantage of this predictability
    - The heap's dynamic allocation patterns are less predictable, making it harder for caching mechanisms to optimize access times.
4. **Allocation and Deallocation Overhead**:
    - Stack memory is managed automatically as functions enter and exit.
    - Heap memory involves more complex bookkeeping than stack memory, contributing to slower access times for heap memory
5. **Fragmentation**: 
    - Over time, the heap can become fragmented as blocks of memory are allocated and freed, leading to gaps between allocated memory areas. This fragmentation can lead to increased search times when the system is trying to find a suitable block of memory to allocate, affecting access times.

```
void functionExample() {
    int *p = new int;   // dynamically allocated int in heap memory
    *p = 10;

    delete p;   // deallocate memory
}
```

### Data Segment
Data segment is composed of 2 parts: 
- **Initialized data segment**: This segment stores global, static, and constant variables with initial values.   
- **Uninitalized data segment**: This segment stores uninitialized global and static variables.

**Initialized Data Segment**:
```
int globalVar = 10;         // global variables
static int staticVar = 10;  // static local variables
const int constVar = 10;    // constant variables with values
```

**Uninitialized Data Segment**:
```
int globalVar;  // uninitialized global variables
```

### Code Segment
Code segment (also known as the Text segment) stores the **executable code (machine code)** of the program. It's usually located in a read-only area of memory to prevent accidental modification
```
void functionExample() {
    // The machine code for this function is stored in the code segment
}
```