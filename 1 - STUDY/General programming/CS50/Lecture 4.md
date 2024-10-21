## Hexadecimal

- Goes from 0 to 9 then A to F

## Pointers

- Is an address.
- Is a value that 'leads me to' another value

```cpp
#include <stdio.h>

int main(void)
{
	int n = 50;
	int* p = &n; // storing the address of 'n' in a variable
	
	printf("%i\n", *p); // accessing the variable inside the address of 'n'

}
```

## Defining custom types
- `typedef` just says to the compiler that those things are "sinonimos"
- 

## Dynamic memory allocation
- In C, we need to include `stdlib.h`
- `malloc` -> stands for "memory allocate". Ask for the compiler to get an certain amount of memory for us. Returns the address of that chunk of memory.
- `free` -> give back the memory used to the computer whenever you finishes using it.
- `strcpy()` -> copy a string.
- `sizeof(int)` -> return the size of an data type, in this case, an integer.

> `VALGRIND` -> useful tool to debug memory allocation, maybe search a little more about it later

- we can use `temporary variables` to swap variables without affecting their original values.
- `overflow` happens when we try to use more memory than we actually have available
## Call stacks
- 

## File pointers
- 

