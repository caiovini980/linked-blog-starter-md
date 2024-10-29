- Data structures are ways of solving problems in a clever way

- `Abstract data type`: a data structure, but if offer some properties that the programmer need to implement them.

- `Linked Lists` is just like an array, but it's not contiguous. It's members can be anywhere in the memory, but each one needs to have a reference to the next address.
  
  It needs an extra pointer to find the first node of the list.
  
  The order of operations are SUPER important.

- `atoi()` stands for "Ascii to integer" and converts a string (or a char*) into a number in C.

- The time of insertion on a linked list is `O(1)`, but the time to search on a linked list is `O(n)`. Because when adding a new value doesn't matter how much items are already in the list, but it matters when we're searching for a value on it.

- `Binary search trees` are just like a linked list but with two pointers per node. And it must be ordered. 
  
  For themselves, they could be a little unbalanced at first, so we need to balance them so they could be `O(log n)` again. Otherwise, they're just a linked list.

- `Hashes` takes a number of inputs and change them to another number of outputs.

```cpp
// Simplest way to implement a hash to return a number between 0 and 25

#include <ctype.h>

int hash(const char* word)
{
	return toupper(word[0]) - 'A';
}
```

- `Tries` is a "tree of arrays". 
  It takes a AMONGUS amount of space to find a word, because it has too much `nullptr`s handing around for each letter of the word.

- `Hash table` is an "array of linked lists"
  
- 

> PRECISO REASSISTIR A EXPLICAÇÃO DE LINKED LIST, não entendi muito bem não