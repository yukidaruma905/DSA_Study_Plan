## Introduction

In C++, the `switch...case` statement is used to perform different actions base on the value of a single expression.

### cpp switch...case Statement

_Syntax:_

```cpp
switch (expression) {
    case constant1:
        /* code to be executed if
        expression is equal to constant1; */
        break;

    case constant2:
        /* code to be executed if
        expression is equal to constant2 */
        break;


    default:
        /* code to be executed if
        expression doesn't match any constant */
}
```

The `expression` is evaluated and compared to the values specified in each `case` statement. 
- If a match is found, the corresponding code block is executed.
- If no match is found, the code in the `default` block is executed.

Notice that the `break` statement is used inside each `case` block. This terminates the `switch` statement.

If the `break` statement is not used, all cases after the correct `case` will be executed, which is NOT what we want!

### Flowchart of switch...case Statement

<figure markdown>
![image](switch_statement_flowchart_dark.svg#only-dark)
![image](switch_statement_flowchart_light.svg#only-light)
    <figcaption>Switch...case Statement Flowchart</figcaption>
</figure>

> **Note:** The expression used in the switch statement can be of type `int`, `char`, `enum` and `string` (c++17 and later) and the case label can be constant expressions like integer, character and enumeration.

Example 1.4.1:

```cpp
#include <iostream>

int main(){
    int x = 2;
    
    switch (x) {
        case 1:
            std::cout << "x is 1" << std::endl;
            break;
        case 2:
            std::cout << "x is 2" << std::endl;
            break;
        case 3:
            std::cout << "x is 3" << std::endl;
            break;
        default:
            std::cout << "x is not 1, 2, or 3" << std::endl;
    }
    
    return 0;
}
```

**Output:**

```
x is 2
```

In this code:

- The variable `x` is assigned the value of `2`.
- Then, the `switch` statement is used to check the value of `x`.
- The `switch` statement checks for a match between the value of `x` and the cases inside the switch statement.
- When a match is found, the corresponding code block is executed.

The `switch` statement is useful when you have a single expression that can have multiple possible values, and you want to perform different actions based on the value of that expression. It's an alternative to multiple `if...else` statements, and it can make your code more readable and efficient.

---