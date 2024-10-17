# Algorithms

- Arrays are continuous on computer memory (back-to-back-to-back)

- Make `sudo code` to get the idea of the implementation first

- In C, we can return from `main()` by returning 0 if everything is ok, or any number if there is a problem

- Big O notation: upper bound
	- `O(n²)`
	- `O(n log n)`
	- `O(n)`: linear time
		- Linear search
	- `O(log n)`
		- Binary search
	- `O(1)`: takes a constant number of steps (doesn't matter the size)
- OMEGA notation: lower bound 
	- `OMEGA(n²)`
	- `OMEGA(n log n)`
	- `OMEGA(n)`
	- `OMEGA(log n)`
	- `OMEGA(1)`: linear search, binary search
- THETA notation: best and worst cases are the same

## Data structures
### struct

```cpp
// structs make possible to create custom data types in C, in C++ we can use classes for that

// `typedef` means "define the following type"

typedef struct
{
	string name;
	string number;
} person;

// the code above creates a new data type named "person"
```

## Linear Search

- Walking in a line on the data structure, checking each item until find what it's looking for, if not, return false.

```cpp
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int numbers[] {20, 500, 10, 5, 100, 1, 50};

	int n = get_int("Number: ");
	for (int i = 0; i < 7; i++)
	{
		if (numbers[i] == n)
		{
			printf("Found!\n");
			return 0;
		}
	}

	printf("Not found!\n");
	return 1;
}
```

- To compare strings, we must use `string.h`

```cpp
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
	string strings[] {"battleship", "boot", "cannon", "iron", "thimble", "top hat"};

	int n = get_int("String: ");
	for (int i = 0; i < 6; i++)
	{
		if (strcmp(strings[i], s) == 0) // strcmp = string compare
		{
			printf("Found!\n");
			return 0;
		}
	}

	printf("Not found!\n");
	return 1;
}
```


## Binary Search

- The idea is to divide and conquer, reducing the search area by half time each time, trying to find a target number.
- To get the middle of the current array, we need to sum the extremes and divide it by 2.
- When the `start` element and the `end` element crossed each other, it means that the searched value isn't on the array.

> The array must be sorted


```cpp
/*
if no slots left
	return false
	
if number is behind middle slot
	return true
	
else if number < middle slot
	search left half
	
else if number > middle slot
	search right half
	
*/
```

## Selection Sort

- O(n²)
- Loop through the data structure `n-1` times, find the smallest number and swap it with the indexed one

## Bubble Sort

- O(n²)
- Really similar to selection sort, but it compares with the next value

```cpp
/*
repeat n-1 times
	for i from 0 to n-2
		if numbers[i] and numbers[i+1] are out of order
			swap them
	
	if no swaps
		quit
*/
```


## Recursion

- A function that calls itself

```cpp
#include <cs50.h>
#include <stdio.h>

void draw(int n);

int main(void)
{
	int height = get_int("Height: ");
	drar(height);
}

void draw(int n)
{
	// if nothing to draw
	if (n <= 0)
	{
		return;
	}
	
	// print pyramid of height n-1
	draw(n - 1);
	
	for (int i = 0; i < n; i++)
	{
		// print one more row
		printf("#");
	}

	printf("\n");
}
```

## Merge Sort

- O (n log n)
- `Log n` means how many times we are "dividing" the data structure.
- When you want to use less time to solve a problem, you have to add more memory to handle it. This sorting tracks more variables, instead of just one.

```cpp
/*
if only one number
	quit
else
	sort left half of numbers
	sort right half of numbers
	merge sorted halves
*/
```

