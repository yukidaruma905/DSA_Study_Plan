## Introduction

In C++, basic input and output can be achieved using the standard input/output library, which includes the following function:

- `cin` (standard input) - reads input from the keyboard.
- `cout` (standard output) - writes output to the screen.
- `cerr` (standard error) - writes error messages to the screen.

### cpp Output

In C++, `cout` sends formatted output to standard output devices, such as the screen. We use the `cout` object along with the `<<` operator for displaying output.

Example 1.1.1:

```cpp
#include <iostream>
using namespace std;

int main() {
	// prints the string enclosed in double quotes
	cout << "Hello World!";
	return 0;
}
```

**Output:**

```
Hello World!
```

> **Note:** if we don't include the `using namespace std;` statement, we need to use `std::cout` instead of `cout`. This is the preferred method as using the `std` namespace can create potential problems.

To print the numbers and character variables, we use the same `cout` object but without using quotation marks.

Example 1.1.2:

```cpp
#include <iostream>

int main() {
	int num1 = 40;
	double num2 = 956.280;
	char ch = 'D';

	std::cout << num1 << endl;  // print integer
	std::cout << num2 << endl;  // print double
	std::cout << "character: " << ch << endl;  // print character
	return 0;
}
```

**Output:**

```
40
956.280
character: D
```

> **Notes:**
> - The `endl` manipulator is used to insert a new line. That's why each output is displayed in a new line.
> - The `<<` operator can be used more than once if we want to print different variables, strings and so on in a single statement.

---
### cpp Input

In C++, `cin` takes formatted input from standard input devices such as the keyboard. We use the `cin` object along with the `>>` operator for taking input.

Example 1.1.3:

```cpp
#include <iostream>
using namespace std;

int main() {
	int num;
	cout << "Enter an integer: ";
	cin >> num;  // Taking input
	cout << "The number is: " << num;
	return 0;
}
```

**Output:**

```
Enter an integer: 40
The number is: 40
```

In the program we used `cin >> num;` to take input from the user. The input is stored in the variable `num`. We then use the `>>` operator with `cin` to take input.

---
#### Taking Multiple Inputs

Example 1.1.4:

```cpp
#include <iostream>

int main() {
	char a;
	int num;

	std::cout << "Enter a character and an integer: ";
	std::cin >> a >> num;

	std::cout << "Character: " << a << std::endl;
	std::cout << "Number: " << num;

	return 0;
}
```

**Output:**

```
Enter a character and an integer: A
29
Character: A
Number: 29
```

---
### cpp Files I/O

C++ provides a standard library called `fstream` (file stream) that contains classes for working with files.

```cpp
#include <iostream>
#include <fstream>
```

There are three classes included in the `fstream` library, which are used to create, write or read files:

| Class      | Description                                                                     |
|:---------- |:------------------------------------------------------------------------------- |
| `ofstream` | Creates and writes to files                                                     |
| `ifstream` | Reads from files                                                                |
| `fstream`  | A combination of `ofstream` and `ifstream`: creates, reads, and writes to files |

#### Create and Write to a File

To create a new file or overwrite an existing file, you can use the `ofstream` class.

_Syntax:_

```cpp
#include <fstream>
...
ofstream outfile;
outfile.open("filename.txt")
```

This creates a new file named "filename.txt" or overwrites an existing file with that name. You can then use the `<<` operator or the `write()` method to write data to the file.

Example 1.1.5:

```cpp
#include <iostream>
#include <fstream>

int main(){
    // Create an ofstream object
    std::ofstream outputFile("output.txt");

    // Write data to the file
    outputFile << "Writing this text to the file" << std::endl;
    outputFile << "This is another line of text" << std::endl;

    // Close the file
    outputFile.close();

    std::cout << "Data has been written to the file" << std::endl;

    return 0;
}
```

This code:

- Creates an object of the `ofstream` class called `outputFile`, wich is used to open file called "output.txt" in the current directory.
- The code then uses the `outputFile` object to write some text to the file, and then closes the file.

#### Read a File

To read data from an existing file, you can use the `ifstream` class.

_Syntax:_

```cpp
#include <fstream>
...
ifstream infile;
infile.open("filename.txt")
```

You can then use the `>>` operator or the `read()` method to read data from the file.

Once you are done working with a file, you should close it using the `close()` method. This releases any resources that were associated with the file and ensures that any changes you made to the file are saved.

It's also worth mentioning that you can check if the file is open or not by checking the `is_open()` method on the file stream variable.

```cpp
if(outfile.is_open()) {
	// file is open and ready for operations
}
```

You can also use `ios::app` flag to open a file in append mode, wich allows you to add data to the end of an existing file without overwriting it.

Example 1.1.6:

First, create the file "input.txt" and place your input like this:

```
This is string
C
23
723.8
```

Then we write our program:

```cpp
#include <iostream>
#include <fstream>
#include <string>

int main(){
    // Create an ifstream object
    std::ifstream inputFile("input.txt");

    // Check if the file could be opened
    if (!inputFile) {
        std::cout << "Error opening file" << std::endl;
        return 1;
    }

    // Read data from the file
    std::string line;
    while (std::getline(inputFile, line)) {
        std::cout << line << std::endl;
    }

    // Close the file
    inputFile.close();

    return 0;
}

```

**Output:**

```
This is string
C
23
723.8
```

This code:

- Creates an object of the `ifstream` class called `inputFile`, which is used to open a file called "input.txt" in the current directory.
- The code then uses an "if" statement to check if the file could be opened successfully.
	- If the file could not be opened, the code prints an error message.
- The code then uses a while loop to read each line of the file using the `getline` function and the `inputFile` object, and it prints each line on the screen.
- Finally, the code closes the file.

> **Note:** Notice that we included a library named `<string>` wich is necessary for the `getline` function that we used in our code.

Working with files in C++ can be a bit more complex than working with simple variables and data structures, but it provides a powerful way to store and retrieve data permanently.

Example 1.1.7:

First, create the file "Files\\inputFile.txt" and place your input like this:

```
6
21.983
H
```

Then we write our program:

```cpp
#include <iostream>
#include <fstream>

int main(){
	// Create ifstream and ofstream objects
	std::ifstream inputFile("Files\\inputFile.txt");
	std::ofstream outputFile("Files\\outputFile.txt");
	
	int x;
	double y;
	char z;
	
	outputFile << "Input Section:" << std::endl;
	outputFile << "Enter an int value: ";
	inputFile >> x;
	outputFile << x << std::endl;
	outputFile << "Enter a double value: ";
	inputFile >> y;
	outputFile << y << std::endl;
	outputFile << "Enter a character: ";
	inputFile >> z;
	outputFile << z << std::endl;
	outputFile << "-------------------------------------" << std::endl;
	
	outputFile << "Output Section:" << std::endl;
	outputFile << "int value is: " << x << std::endl;
	outputFile << "double value is: " << y << std::endl;
	outputFile << "character value is: " << z << std::endl;
	outputFile << "-------------------------------------" << std::endl;
	
	// Close the files 
	inputFile.close(); 
	outputFile.close();
	
	return 0;
}
```

**Output:**

```
Input Section:
Enter an int value: 6
Enter a double value: 21.983
Enter a character: H
-------------------------------------
Output Section:
int value is: 6
double value is: 21.983
character value is: H
-------------------------------------
```

This code is a basic example of reading and writing data to and from files in C++. 

The code:

- Includes two libraries, `iostream` and `fstream`, which are used for input/output operations.
- In the `main` function, two objects, `inputFile` and `outputFile`, are created using the `ifstream` and `ofstream` classes respectively. These objects are used to open two files, `inputFile.txt` and `outputFile.txt`, that are located in a directory called "Files".
- The code then declares three variables, `x`, `y`, and `z`, which are used to store the input data read from the input file.
- The `outputFile` object is then used to write some text to the output file, including prompts for the user to enter an integer, double, and character, respectively.
- The `inputFile` object is then used to read these values from the input file, which are then written to the output file using the `outputFile` object.
- Finally, the code closes both files and return 0 to indicate successful execution.

> **Note:** That you need to create the `inputFile.txt` with the necessary input before running your code.


---