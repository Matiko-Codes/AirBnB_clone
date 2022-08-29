# AirBnB clone - The console
![HNBN](https://ibb.co/86nPd8P)
---
## Command Line Interpreter
This is the first step towards our first full web application: the **AirBnB clone**. This step is important because we will use it with other upcoming projects i.e HTML/CSS templating, database storage, API, front-end intergration...
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
