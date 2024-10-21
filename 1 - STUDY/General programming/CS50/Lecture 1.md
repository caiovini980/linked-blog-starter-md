- `Source code` is the code itself

- `Compiler` is what convert from a language to another\

- `Machine code` is the source code converted to binary by the compiler so the computer could understand

- `#include` says to the compiler to search for some file, copy it and paste it on the file calling the include

- Relevant link to serve as a little documentation for C: https://manual.cs50.io/ 

- List of format codes:
	- `%s`  -> strings
	- `%i`  -> integers
	- `%c`  -> chars
	- `%f`  -> floats
	- `%li` -> signed longs
	- `%lu` -> unsigned longs
	- `%p` -> show an address

- Always that you're writing a new project, follow the code guidelines pre defined by the team. If you're working alone, is the same principle. 
  
  On GitHub, remember to put these guidelines on the Readme file of your project. This don't need to be really complex, it could be just some lines to define how your source code will be structured (visually)

- When we use a single character on a string, or a char, we should use `''`. If is a multiple character string, we should use `""`

- Normally don't use the same variable naming on different scopes

- Command for files in Command-line:
	- `cd` -> 'change directory'
	- `mv` -> move file
	- `cp` -> copy file
	- `rm` -> remove file
	- `ls` -> list files on the current folder
	- `mkdir` -> make a new directory (folder) 
	- `rmdir` -> remove a directory

- Truncation: if you divide a integer by an integer, the decimal points will be thrown away.
	- A way to solving this is `type casting` to treat the integer as a float (or double)

- Use `%f` for doubles (32 bits) and doubles (64 bits)

- Floating point imprecision: we cannot represent an infinite amount of numbers with a finite amount of memory