## Introduction

In C++, data types are used to define the type of a variable, which determines the size and layout of the variable's memory, as well as the set of operations that can be performed on it.

---
### cpp Fundamental Data Types

The table below shows the fundamental data types, their meaning, and their sizes (_in bytes_):

| Data Types | Meaning               | Size (_in Bytes_) |
|:---------- |:--------------------- |:-----------------:|
| `int`      | Integer               |      2 or 4       |
| `float`    | Floating-point        |         4         |
| `double`   | Double Floating-point |         8         |
| `char`     | Character             |         1         |
| `wchar_t`  | Wide Character        |         2         |
| `bool`     | Boolean               |         1         |
| `void`     | Empty                 |         0         |

---
### cpp Type Modifiers

We can further modify some of the fundamental data types by using types modifiers.

There are 4 types modifiers in C++. These are:

1. `signed`
2. `unsigned`
3. `short`
4. `long`

We can modify the following types with the above modifiers:

- `int`
- `double`
- `char`

#### cpp Modifiers Data Types List

| Data Type            | Size (_in Bytes_) | Meaning                                                                  |
|:-------------------- |:-----------------:|:------------------------------------------------------------------------ |
| `signed int`         |         4         | used for integers (equivalent to int)                                    |
| `unsigned int`       |         4         | can only store positive integers                                         |
| `short`              |         2         | used for small integers (range -32768 to 32767)                          |
| `unsigned short`     |         2         | used for small integers (range 0 to 65,535)                              |
| `long`               |    at least 4     | used for large integers (equivalent to long int)                         |
| `unsigned long`      |         4         | used for large positive integers or 0 (equivalent to unsigned long int)  |
| `long long`          |         8         | used for very large integers (equivalent to long long int)               |
| `unsigned long long` |         8         | used for very large integers or 0 (equivalent to unsigned long long int) |
| `long double`        |        12         | used for large floating-point numbers                                    |
| `singed char`        |         1         | used for character (guaranteed range -127 to 127)                        |
| `unsigned char`      |         1         | used for characters (range 0 to 255)                                     |

Let's see a few examples:

Example 1.2.1:

```cpp
long b = 4523232;
long int c = 2345342;
long double d = 233434.56343;
short d = 3434233; // Error! out of range
unsigned int a = -5;    // Error! can only store positive numbers or 0
```

---
#### Auto specifier

The `auto` specifier is a way of detecting the data type base on assignment value.

Example 1.2.2:

```cpp
auto i = 5;   // causes i to be of type int
              // and
auto j = 5.0; // causes j to be of type double.
```

### Derived Data Types

- arrays.
- pointers.
- function types.
- structures.

---