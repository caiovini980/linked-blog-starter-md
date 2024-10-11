
### Flyweight
This patterns consists in separating out an object's data into two kinds:
- Intrinsic State:
	- Stuff that is not specific to a single instance of that object and can be shared across all of them
	- Context-free stuff
- Extrinsic State:
	- Stuff that is unique to an instance, like position rotation and scale of a mesh.

---
### Command
This patters consists in separating parts of the code into "actions", or "commands" that could be easily swapped when needed. 
A example for that is the Unreal's new Input System, based on Actions and Action Mappings (which action each input will be responsible for, and this can be changed easily).

```cpp
// we define a base clas that represents a triggerable game command
class Command
{
public:
	virtual ~Command();
	virtual void execute() = 0;
};

// Then we create subclasses for each of the different game actions
#include "Command.h"
class JumpCommand : public Command
{
public: 
	virtual void execute() 
	{ 
		jump(); 
	}
};

#include "Command.h"
class FireCommand : public Command
{
public: 
	virtual void execute() 
	{ 
		fireFun(); 
	}
};

// In our our output handler, we store a pointer to a command for each button
#include "Command.h"
class InputHandler
{
public:
	void handleInput();

private:
	Command* buttonX;
	Command* buttonY;
	Command* buttonA;
	Command* buttonB;
}
```

```cpp
// On the InputHandler.cpp file
void InputHandler::handleInput()
{
	if (isPressed(BUTTON_X))
	{
		buttonX->execute();
	}
	else if (isPressed(BUTTON_Y))
	{
		buttonY->execute();
	}
	else if (isPressed(BUTTON_A))
	{
		buttonA->execute();
	}
	else if (isPressed(BUTTON_B))
	{
		buttonB->execute();
	}
}
```

We can also pass the object we wanted to execute that command, something like:
```cpp
class Command
{
public:
	virtual ~Command();
	virtual void execute(GameActor& actor) = 0;
}
```