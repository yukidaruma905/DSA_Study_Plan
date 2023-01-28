## Introduction

An array is a collection of elements of the same data type, stored in contiguous memory locations. Arrays are used to store multiple values of the same type in a single variable.

---
### cpp Array Declaration

_Syntax:_

```cpp
dataType arrayName[arraySize];
```

Example 1.4.1:

```cpp
int x[6];
```

Here,

- `int` - type of element to be stored.
- `x` - name of the array.
- `6` - size of the array.

---
### Access Elements in cpp Array

In C++, each element in an array is associated with a number. The number is known as an array index. We can access elements of an array by using those indices.

_Syntax:_

```cpp
// syntax to access array elements
array[index];
```

Consider the array `x` we have seen above:

<figure markdown>
![image](array_1_dark.svg#only-dark)
![image](array_1_light.svg#only-light)
    <figcaption>Array's Index</figcaption>
</figure>


Few things to remember

- The array indices start with `0`. Meaning `x[0]` is the first element stored at index `0`.
- If the size of an array is `n`, the last element is stored at index `(n-1)`. In this example, `x[5]` is the last element.
- Elements of an array have consecutive addresses. For example, suppose the starting address of `x[0]` is 2120d. Then, the address of the next element `x[1]` will be 2124d, the address of `x[2]` will be 2128d and so on.

Here, the size of each element has increased by 4. This is because the size of `int` is 4 bytes.

Example 1.5.1:

```cpp
#include <iostream>

int main(){
    // Declare an array of size 5
    int myArray[5];
    
    // Assign values to the array
    myArray[0] = 1;
    myArray[1] = 2;
    myArray[2] = 3;
    myArray[3] = 4;
    myArray[4] = 5;
    
    // Print the values of the array
    for (int i = 0; i < 5; i++) {
        std::cout << "myArray[" << i << "]: " << myArray[i] << std::endl;
    }
    
    return 0;
}
```

**Output:**

```
myArray[0]: 1
myArray[1]: 2
myArray[2]: 3
myArray[3]: 4
myArray[4]: 5
```

In this code:

- An array called `myArray` is declared with a size of `5`.
- Then, values are assigned to each element of the array using the array index.
- Finally, a `for` loop is used to print the values of the array.

---
### cpp Array Initialization

In C++, it's possible to initialize an array during declaration.

_Syntax:_

```cpp
// declare and initialize an array
dataType arrayName[arraySize] = {element1, element2, ....};
```

<figure markdown>
![image](array_2_dark.svg#only-dark)
![image](array_2_light.svg#only-light)
    <figcaption>Array initialization</figcaption>
</figure>

Another method to initialize array is during declaration:

```cpp
dataType arrayName[] = {element1, element2, ....};
```

Here, we have not mentioned the size of the array. In such cases, the compiler automatically computes the size.

Example 1.5.2:

```cpp
#include <iostream>

int main(){
    // Declare and initialize an array
    int myArray[] = {1, 2, 3, 4, 5};
    
    // Print the values of the array
    for (int i = 0; i < 5; i++) {
        std::cout << "myArray[" << i << "]: " << myArray[i] << std::endl;
    }
    
    return 0;
}
```

**Output:**

```
myArray[0]: 1
myArray[1]: 2
myArray[2]: 3
myArray[3]: 4
myArray[4]: 5
```

This code is the same as the one before, only in here we used the `{}` notation to initialize an array with a set of values while declaring it.

---
### cpp Array With Empty Members

In C++, if an array has a size of `n`, we can store up to `n` number of elements in the array. However, what will happen if we store less than `n` number of elements?

In such cases, the compiler assigns random values to the remaining places.

Oftentimes, this random value is simply `0`.

<figure markdown>
![image](array_3_dark.svg#only-dark)
![image](array_3_light.svg#only-light)
    <figcaption>Array padding empty members</figcaption>
</figure>

---
### cpp Array Out of Bounds

If we declare an array of size `10`, then the array will contain elements from index `0` to `9`.

However, if we try to access the element at index `10` or more than `10`, it will result in an "Undefined Behavior".


---