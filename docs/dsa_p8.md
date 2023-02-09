## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=n;i>=1;i--) {
		for(int j=1;j<=n-i;j++) {
			std::cout << " ";
		}
		for(int j=0;j<2*i - 1;j++) {
			std::cout << "*";
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
*********
 *******
  *****
   ***
    *
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the pyramid height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from (`n` to `1`), this will handle the height of the pattern, and the inner loop `j` runs from (`1` to `n-i`) for each iteration of the outer loop.
	- This loop is used to print the white-space characters `" "` to indent the asterisks to the right.
	- The number of white-spaces printed in each row is calculated using the expression `n-i`.
	- For example, when the algorithm is running in the third row `i=3` the number of white-spaces is `n-i=2`.
- After printing the white spaces, another nested loop runs `2*i-1` number of times to print the asterisk `*` to form the pyramid shape
- The number of asterisks printed in each row is calculated using the expression `2*i-1`.
	- For example, when the algorithm is running in the first row `i=5`, the number of asterisks that we need to print is `2*i-1=9`.
	- when the algorithm is running in the second row `i=4`, the number of asterisks that we need to print is `2*i-1=7`, and so on.
- After the inner loops are finished, a call to `std::cout << std::endl;` is made to move the cursor to the next line in the console, thus allowing the next row of the pyramid to be printed on a new line.
- The outer loop continues to run `n` number of times until `i` is equal to `1`.

---