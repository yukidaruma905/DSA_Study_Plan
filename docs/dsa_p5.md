## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=n;i>=1;i--) {
		for(int j=1;j<=i;j++) {
			std::cout << "*";
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
*****
****
***
**
*
```

In this code:

- We need to print a right-triangle pattern of asterisks (`*`), but with the rows starting from the highest value of `n` (number of rows) and decrementing down to `1`.
- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`n` to `1`), this will handle the height of the pattern, and the inner loop `j` runs from (`1` to `i`) for each iteration of the outer loop.
	- we start counting backwards, the first line value is `5`. so, we need to print the asterisks sign five times.
	- the second line value is `4`. so, we print the asterisks sign four times, and so on.
- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and a right-triangle pattern of asterisks is printed to the console with the rows starting from the highest value of `n` (5) and decrementing down to `1`.

---