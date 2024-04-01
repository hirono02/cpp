# Reference
A reference can be considered as a constant pointer which always points to (references) the same object. They are declared using the `&` symbol

### Declaration and Initialization
To declare a reference, we should use the `&` symbol followed by the variable type and the reference's name. Note that we must initialize a reference when we declare it.   
```
int var = 10;   // declare an integer variable
int &ref = var; // declare a reference that "points to/refer to" var
```

### Usage
We can use the reference just like we would use the original variable. When we change the value of the reference, the value of the original variable also changes, because they both share the same memory location.   
```
int var = 10;
int &ref = var;

var = 20;   
std::cout << ref << std::endl;  // outputs 20

ref = 30;
std::cout << var << std::endl;  // outputs 30
```

### Function parameters
We can use references as function parameters to create an alias for an argument. This is commonly done when we need to modify the original variable or when passing an object of considerable size to avoid the cost of copying.   
```
void swap(int &a, int &b) {
    int temp = a;
    a = b;
    b = temp;
}

int main() {
    int x = 5, y = 10;
    std::cout <<"Before swap: x = " << x << " and y = " << std::endl;   // x = 5, y = 10

    swap(x, y);
    std::cout <<"After swap: x = " << x << " and y = " << std::endl;    // x = 10, y = 5

    return 0;
}
```