- When we are compiling through command-line, we need to specify to the compiler what libraries we're using.

- Every line in C/C++ starting with `#` is a 'preprocessor directive'.

- The compiler converts C (or the used language) into Assembly

- Compiling
	- Preprocessing: Converts all the `macros` into their related definitions.
	- Compiling: Converts the C code into Assembly.
	- Assembling: Get the assembly code and converts into machine code (binary).
	- Linking: Get all the assemblies and link them together into a single file (normally the output file).

- `clang` is more modern, and better, than `gcc`.

- Toolkit for `debugging`
	- Print on the screen
		- Always delete the temporary prints
	- Use the debugger
		- Always prefer to use the debugger instead of print
	- Read through your code talking out loud to some object (rubber duck debugging)
	- 

- Primitive sizes (bytes):
	- bool: 1
	- int: 4
	- long: 8
	- float: 4
	- double: 8
	- char: 1
	- string: ? (vary accordingly with the amount of text used)

> Math operations using only integers, will result in only integers.
## Strings

- Strings are just arrays of characters

```cpp
string word { "Hello!" };
// is equal to
char wordChar[] { "Hello!" };
```

- Every string have a character at the end of it that represents the point where the compiler should stop reading that string, this point is the `\0` (or a `null` byte, where every bit is 0)

```cpp
char word[] { "Hello!" }; 
/* 
	-> we can access each letter separately, like:
	
	word[0] = "H";
	word[1] = "e";
	word[2] = "l";
	word[3] = "l";
	word[4] = "o";
	word[5] = "!";
	
	-> BUT, we can also get the endpoint for that string 
	on the very last slot of the array:
	
	word[6] = "\0";
*/
```

- An array of strings is basically a bidimensional array of chars.

## Command-line arguments
- We can access the information sent to the compiler, when running the program through command-line, though the `argv` parameter of the `main()` function. 

> OBS: The information at the index 0 will always be the name of the program

```cpp
#include <stdio.h>

int main(int argc, string argv[]) 
{
	// 'argc' -> argument counts
	// 'argv' -> argument vector (list of command-line arguments)
}
```


