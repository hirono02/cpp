# Static Arrays
Arrays are a way of storing data *contiguously*. In stricly type languages like Java and C++, arrays have an allocated size when initialized. This means taht the size of an array cannot be changeed after its initialization.  

The most common array operations are:
- Reading
- Deletion
- Insertion

### Reading from an array
Array elements are accessed through **indices**, which starts at 0 in most languages. Reading from an array is as simple as accessing the index. 
```
// initialize myArray
 int myArr[3] = {1, 3 ,4};

// access an arbitrary element, where i is the index of the desired value
myArray[i];
```