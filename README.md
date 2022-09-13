# AirBnB clone - The console
![HNBN](https://github.com/Matiko-Codes/AirBnB_clone/blob/main/65f4a1dd9c51265f49d0.png)
---
## Command Line Interpreter
This is the first step toward our first full web application: the **AirBnB clone**. This step is important because we will use it with other upcoming projects i.e HTML/CSS templating, database storage, API, front-end intergration...
Each task is designed to help us:
* Create a parent class called `BaseModel`. This will take care of initialization, serialization and deserialization of our future instances.
* Create a simple flow of serialization/deserialization: `Instance<-> Dictionary <-> JSON string <-> file`
* Create all classes used for AirBnB (`User`, `State`, `City`, `Place`...) that inherit from `BaseModel`
* Create the first abstracted storage engine of the project: File storage.
* Create all unittests to validate all our classes and storage engine.
---
## What is a command interpreter?
Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

* Create a new object (ex: a new User or a new Place)
* Retrieve an object from a file, a database etc…
* Do operations on objects (count, compute stats, etc…)
* Update attributes of an object
* Destroy an object
---
### Description of the command interpreter
|    Commands                          |             Description                          |
|:-------------------------------------|:-------------------------------------------------|
|`quit`                  | Quits the console                  |
|`CTRL + D`              | Quits the console                  |
|`help` or `help<command>`|Displays all commands or Displays instructions for a specific command|
|`update <class> <id> <attribute name> "<attribute value>"`|Updates an object with a certain attribute (new or existing)|
|`create <class>`|Creates an object of type , saves it to a JSON file, and prints the objects ID|
|`show <class> <ID>`|Shows string representation of an object|
|`destroy <class> <ID>`|Deletes all objects|
|`all` or `all <class>`|Prints all string representations of all objects or Prints all string representations of all objects of a specific class|
|`<class>.all()`|Same as `all <class>`|
|`<class>.count()`|Retrieves the number of objects of a certain class|
|`<class>.show(<ID>)`|Same as `show <class> <ID>`|
|`<class>.destroy(<ID>)`|Same as `destroy <class> <ID>`|
|`<class>.update(<ID>, <attribute name>, <attribute value>`|Same as `update <class> <ID> <attribute name> <attribute value>`|
|`<class>.update(<ID>, <dictionary representation>)`|Updates an objects based on a dictionary representation of attribute names and values|
### Execution
This how our shell should work like in an interactive mode:

```shell
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$
```

But also in non-interactive mode:(Like in Shell Project in C)

```shell
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
```

	All tests should also pass in non-interactive mode: `$ echo "python3 -m unittest discover tests" | bash`
	//This work was a team work basic intro to creating a final project 
