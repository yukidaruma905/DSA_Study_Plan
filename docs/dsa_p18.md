## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=0;i<n;i++) {
		for(int j=0;j<=i;j++) {
			std::cout << (char)('A'+n-1-j);
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
E
ED
EDC
EDCB
EDCBA
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the right-triangle height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`0` to `n-1`), this will handle the height of the pattern, and the inner loop `j` runs from (`0` to `i`) for each iteration of the outer loop, this will control the number of letters in each row.
- In the inner `for` loop, the code `std::cout << (char)('A' + n - 1 - j)` is used to print out the letters of the triangle.
	- The `n - 1 - j` term calculates the position of the letter in the alphabet sequence.
	- `'A'` is added to make the starting letter `'A'`
	- The `(char)` typecast is used to convert the result of the expression to a character and print it to the console.
- After printing each row of letters, a new line is started using `std::cout << std::endl;`.

---