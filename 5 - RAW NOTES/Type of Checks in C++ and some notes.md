- `ComPtr` - Really similar to `shared_ptr` but specific to Microsoft 

```cpp

// Check if a class has a parent of a specific class using template

// The next line check during pre-compilation time
template<typename T, typename = std::enable_if_t<std::is_base_of_v<Character, T>>> 
T* CreateCharacter(std::string name, int x, int y) 
{ 
	// The static assert check during compilation time
	static_assert(std::is_base_of_v<Character, T>, "T should inherit from Character"); 
	
	T* newCharacter = new T(name, x, y); _characters.push_back(newCharacter); 
	
	return newCharacter; 
} 

std::vector<Character*> _characters;

```

```cpp

// Example of a template being applied to the example above for readability
#define BaseOf(A, T) typename = std::enable_if_t<std::is_base_of_v<A, T>>
template<typename T, BaseOf(Character, T)>

```

