## Solution

```cpp
#include <iostream>

int n=5;

int main(){
	for(int i=1;i<=n;i++) {
		for(int j=1;j<=n-i;j++) {
			std::cout << " ";
		}
		for(int j=0;j<2*i - 1;j++) {
			std::cout<<"*";
		}
		std::cout << std::endl;
	}
	return 0;
}
```

**Output:**

```
    *
   ***
  *****
 *******
*********
```

In this code:

- The first line of code sets the value of an integer variable `n` to `5` (where `n` is the pyramid height or the number of rows).
- In the `main` function, there are two nested `for` loops. The outer loop `i` runs from `1` to `n` (`1` to `n`), this will handle the height of the pattern, and the inner loop `j` runs from `1` to `n-1` for each iteration of the outer loop.
- Inside the inner loop, the statement `std::cout << " ";` prints a space character to the console. The number of spaces printed depends on the value of `n` and the current iteration of the outer loop.
	- when the algorithm is running in the first row `i=1` the number of white-spaces `" "` is `n-i=4`, this sets the center of the pyramid 4 places to the right in order to give the pyramid its shape on the console.
	- when the algorithm is running in the second row `i=2` the number of white-spaces `" "` is `n-i=3`, and so on.
- The second inner loop `j` runs from `0` to `2*i-1` for each iteration of the outer loop.
	- when the algorithm is running in the first row `i=1` the number of asterisks that we need to print is `2*i-1=1`, this will print the pointed head of the pyramid.
	- when the algorithm is running in the second row `i=2` the number of asterisks that we need to print is `2*i-1=3`, this will reprint the center line and adds two more (one on the right and one on the left, thus giving the illusion of printing a pyramid), and so on.
- After the inner loops finish executing, the statement `std::cout << std::endl;` prints a newline character, which causes the program to print a new line for the next iteration of the outer loop.
- This process repeats until both loops have finished executing, and pyramid pattern of asterisks (`*`) with the height of `n` is printed to the console.

---