## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=n;i>=1;i--) {
		for(int j=1;j<=i;j++) {
			std::cout << j;
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
12345
1234
123
12
1
```

In this code:

- Like the previous program, this one also prints a right-triangle pattern, but instead of asterisks (`*`), it prints numbers.
- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from `n` to `1` (`5` to `1`), this will handle the height of the pattern, and the inner loop `j` runs from `1` to `i` (`1` to `i`) for each iteration of the outer loop.
- Inside the inner loop, the statement `std::cout << j;` prints the value of `j` to the console (the number of column).
	- when the algorithm is running in the second row `i=4`, we need to print the value of the first `4` columns to the console `1 2 3 4`.
	- when the algorithm is running in the third row `i=3`, we need to print the number of the first `3` columns to the console `1 2 3`.
- After the inner loop finishes executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and a right-triangle pattern of asterisks is printed to the console with the rows starting from the highest value of `n` (5) and decrementing down to `1`.

---