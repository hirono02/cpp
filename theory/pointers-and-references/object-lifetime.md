# Object Lifetime in C++
Object lifetime refers to the time during which an object exists, from the moment it is created until it is destroyed. In C++, an object's lifetime can be classified into four categories:

1. [Static Storage Duration](#static-storage-duration)
2. [Threat Storage Duration](#thread-storage-duration)
3. [Automatic Storage Duration](#automatic-storage-duration)
4. [Dynamic Storage Duration](#dynamic-storage-duration)

### Static Storage Duration
Objects with static storage duration exist for the **entire** run of the program. These objects are allocated at the beginning of the program's run and deallocated when the program terminates. Global variables, static data members, and static local variables fall into this category
```
int global_var;              // static storage duration
class myClass {
    static int static_var;   // static storage duration
}
void myFunction() {
    static int local_var;    // static storage duration
}
```

### Thread Storage Duration
Objects with thread storage duration exist for the lifetime of the thread they belong to. They are created when a thread starts and destroyed when the thread exits. Thread storage duration can be specified using the `thread_local` keyword
```
thread_local int my_var;     // thread storage duration
```

### Automatic Storage Duration
Objects with automatic storage duration are created at the point of definition and destroyed when the scope in which they are declared is exited. These objects are also known as **local** or **stack** objects. Function parameters and local non-static variables fall into this category
```
void myFunction() {
    int local_var;          // automatic storage duration
}
```

### Dynamic Storage Duration
Objects with dynamic storage duration are created at runtime, using memory allocation functions such as `new` or `malloc`. The lifetime of these objects must be managed manually, as they are not automatically deallocated when the scope is exited. It is the programmer's responsibility to destory the objects using the `delete` or `free` functions when they are no longer needed, to avoid memory leaks
```
int *ptr = new int;         // dynamic storage duration
delete ptr;                 // deallocating memory
```

Understanding object lifetime is essential for efficiently managing memory in C++ programs and avoiding common issues such as memory leaks and undefined behaviour