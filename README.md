#0x00. AirBnB clone - The console project

#PROJECT DESCRIPTION
This is the 0x00 Airbnb project the first project aimed at creating my first website through backend
engineering using python and console application and cmd module

#DESCRIPTION FOR THE COMMAND INTERPRETER
the commnd interpreter serves as the fronend of the web application users can also interact with the
backend wich has been developed with the python OOP program
the interface of the program has been developed to work similarly to the bash shell only that this
project has limited number of commands that are only meant for the project

some of the available commands are;
#Show
#Create
#Update
#Destroy
#Count

some of the actions that can be performed
Creating new objects (ex: a new User or a new Place)
Retrieving an object from a file, a database etc…
Doing operations on objects (count, compute stats, etc…)
Updating attributes of an object
Destroying an object

#HOW TO START IT
#Instalation
cloning the repo of the project from github account the repo contains the whole simple shell program
and its dependencies

/**

#git clone git@github.com:Smolclin/AirBnB_clone.git

**/

after the cloning of the repo, you will have a folder called AirBnB_clone which contains files which
helps in running the program

#such file are;
console.py : The main executable of the project, the command interpreter.
models/engine/file_storage.py: Class that serializes instances to a JSON file and deserializes JSON file to instances
 
models/__ init __.py:  A unique `FileStorage` instance for the application
 
models/base_model.py: Class that defines all common attributes/methods for other classes.
 
models/user.py: User class that inherits from BaseModel
 
models/state.py: State class that inherits from BaseModel

models/city.py: City class that inherits from BaseModel

models/amenity.py: Amenity class that inherits from BaseModel

models/place.py: Place class that inherits from BaseModel

models/review.py: Review class that inherits from BaseModel

#HOW TO USE IT
works in two diffrent modes
namely interactive and Non-interactive mode
in interactive; the console displays a prompt(hbnb) for the user to write and  execute a command in which
it runs through loop untill the program is exited

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

in non-interactive mode; here the shell id run with a commnd input piped into its execution so that the
command is run whenever the shell is started

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

#the command input format

to give the commands to the consol there is piping through an echo in case of non-interctive mode

incase of interactive mode; here commands are written using the keyboard and ehnever the prompt appears
it is recognized when an enter key is pressed. the console attempts to execute the command and returns an
error whenever the command is not executed
exiting the console can be done using 'CTRL + D', 'CTRL + C' or command 'quit' or 'EOF'

#arguements
for the shell to understand the parameters the user should separate the arguements using space

example

**
user@ubuntu:~/AirBnB$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
user@ubuntu:~/AirBnB$ ./console.py

**

or

**
user@ubuntu:~/AirBnB$ ./console.py $ echo "create BaseModel" | ./console.py
(hbnb)
e37ebcd3-f8e1-4c1f-8095-7a019070b1fa
(hbnb)
user@ubuntu:~/AirBnB$ ./console.py

**

#available commands and their work

|Command| Description |
|--|--|
| **quit or EOF** | Exits the program |
| **Usage** | By itself |
| **-----** | **-----** |
| **help** | Provides a text describing how to use a command.  |
| **Usage** | By itself --or-- **help <command\>** |
| **-----** | **-----** |
| **create** | Creates a new instance of a valid `Class`, saves it (to the JSON file) and prints the `id`.  Valid classes are: BaseModel, User, State, City, Amenity, Place, Review. |
| **Usage** | **create <class name\>**|
| **-----** | **-----** |
| **show** | Prints the string representation of an instance based on the class name and `id`  |
| **Usage** | **show <class name\> <id\>** --or-- **<class name\>.show(<id\>)**|
| **-----** | **-----** |
| **destroy** | Deletes an instance based on the class name and `id` (saves the change into a JSON file).  |
| **Usage** | **destroy <class name\> <id\>** --or-- **<class name>.destroy(<id>)** |
| **-----** | **-----** |
| **all** | Prints all string representation of all instances based or not on the class name.  |
| **Usage** | By itself or **all <class name\>** --or-- **<class name\>.all()** |
| **-----** | **-----** |
| **update** | Updates an instance based on the class name and `id` by adding or updating attribute (saves the changes into a JSON file).  |
| **Usage** | **update <class name\> <id\> <attribute name\> "<attribute value\>"** ---or--- **<class name\>.update(<id\>, <attribute name\>, <attribute value\>)** --or-- **<class name\>.update(<id\>, <dictionary representation\>)**|
| **-----** | **-----** |
| **count** | Retrieve the number of instances of a class.  |
| **Usage** | **<class name\>.count()** |

#Auther

CLINTON OTIENO
