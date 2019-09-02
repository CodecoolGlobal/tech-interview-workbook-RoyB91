# Programming Basics questions

## Computer science

### Data structures

#### What is the purpose and working method of a list/array data structure?
> An array is a collection of items stored at contiguous memory locations. 
The idea is to store multiple items of the same type together. Find them easier.
The Data Structure can be implemented in several ways and its implementation may vary from language to language.
#### What is the difference between a list/array and a set?
>List is an ordered sequence of elements whereas Set is a distinct list of elements which is unordered.
Set contains no duplicate elements.
#### What can you tell about the stack and queue data structure?
>Stack A stack is a linear data structure in which elements can be inserted and deleted only from one side of the list, called the top.
A stack follows the LIFO (Last In First Out) principle, i.e., the element inserted at the last is the first element to come out.
The insertion of an element into stack is called push operation, and deletion of an element from the stack is called pop operation.
In stack we always keep track of the last element present in the list with a pointer called top.
#### What is the purpose and working method of a dictionary/map data structure?
>A dict can be thought of as a container of ( key : value ) pairs. This can be a helpful way to imagine the information in a mapping.
Each pair in the list is the mapping from a key to an associated value.
Faster method for look for,

### Algorithms

#### Fibonacci sequences. Write a method(or pseudo code), that generates the Fibonacci sequences.
```python
def fibonacci(n):
    a = 0
    b = 1
    for i in range(0, n):
        temp = a
        a = b
        b = temp + b
    return a
    
for c in range(0, 15):
    print(fibonacci(c))  
```       
#### How do you find a max value in a list/array if you can’t use any built-in functions?
> I check the elements one by one in a cycle till the end of the list/array length , and
meanwhile i compare the elements with each others and always checking the next element,
with the previous higher one.

#### What do we call an *in-place* sort?
>An in-place sorting algorithm uses constant extra space for producing the output (modifies the given array only). It sorts the list only by modifying the order of the elements within the list.

### Programming paradigms - procedural

#### What is “Stack overflow”? Write a code, that ends up with stack overflow. What is the call stack?
>Stack Over flow is basically a phenomenon or programming mistake that occurs, when the computer or processor memory (often called stack), is filled more than its stack capacity. Then the stack overflows leading to loss of elements in memory. You end up losing the foremost or recent element. 
```python
def stack_overflow():
    return stack_overflow()
    
stack_overflow()

"by building an infinately recursive funcion"
```
#### What is the function signature?
>A function signature (or type signature, or method signature) defines input and output of functions or methods.
 A signature can include: parameters and their types.
 a return value and type. exceptions that might be thrown or passed back.

### Programming languages - Python
#### How do you use a dictionary in Python?
>I am working with key,value pairs. 
#### What does it mean that an object is Immutable in Python?
> You cant change the original object if you want to work with it, u have to assign 
it to a new object.(eg. list)
#### What is conditional expression in Python?
>The If/else.
```python
x = 20

if x < 50:
    print('(first suite)')
    print('x is small')
else:
    print('(second suite)')
    print('x is large')
```
#### What are different types of arguments in Python?
>Arguments are the values that are passed to the function at run-time so that the function can do the designated task using these values.

#### What is variable shadowing? (context: variable scope)
> variable shadowing occurs when a variable declared within a certain scope (decision block, method, or inner class) has the same name as a variable declared in an outer scope.
#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
>You can do that freely.
#### What happens if you try to add an item to the end of a List, while you are iterating over it in Python?
>You can do that freely.
#### What is the "golden rule" of variable scoping in Python? What is the lifetime of variables?
>If its possible , do not use global variable.
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
> i can assign it to a new variable outside in a loop.
#### What type of elements can a list contain in Python?
>integer,string(nearly every type)
#### What is slicing in Python?
>You can divide a String/List with slicing.(eg: you can slice a list by its index)
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
>Basic Operators in Python. Arithmetic operators: Arithmetic operators are used to perform mathematical operations like addition,
subtraction, multiplication and division.
 
#### What is the purpose of the in and not in membership operators in Python?
> You can check the elements if its exist in array/list or not.
#### What does the + operator mean when used with strings in Python?
> You can add string to each other.(eg; "A" + "B" = "AB")
#### How do you format strings in Python with the format() function?
>f(string)
#### Name 4 iterable types in Python!
>iter(), for loop, 
#### What is the difference between list, set, dictionary comprehension and a generator expression in Python?
A List Comprehension, just like the plain range function, executes immediately and returns a list.

A Generator Expression, just like xrange returns and object that can be iterated over.

The comparision is not perfect though, because in an object returned by the generator expression, we cannot access an element by index.
>The difference between the two kinds of expressions is that the List comprehension is enclosed in square brackets [] while the Generator expression is enclosed in plain parentheses ().
#### Does the order of the function definitions matter in Python? Why?
>>It doesn't matter in which order the functions are created. It only matters when the call to the function is done
#### What is the difference between input parameters and local variables in Python?
>At the input parameters the function waiting for a parameter to run. While the local
variables are constants.
#### What does unpacking mean in Python?
Unpacking is used to pass list or dictinary at its element level.
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?
>You have to use return statement, when u want to use the result in other functions.
#### What is the difference between positional and keyword parameters in Python?
A keyword argument is just a positional argument with a default value. You must specify all arguments that don't have a default value. In other words,
keyword arguments are only "optional" because they will be set to their default value if not specifically supplied.

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
>You can use debugging feature by IDE. (Or if its small application you can printing)
#### What does step over, step into and step out mean while using the debugger?
> You can jump through a step , or jump in and check one by one in the program.And where
should close the debug.
#### How can you start the program from a certain line using the debugger? (careful, tricky! :) )
>If u using an IDE, u can just a red circle next to the line number.
### Version control

#### What are the advantages of using a version control system?
>Easier to handle the whole project.
#### What is the difference between the working directory, the staging area and the repository in git?
Working directory:
>The working directory is a single checkout of one version of the project. These files are pulled out of the compressed
database in the Git directory and placed on disk for you to use or modify.

Staging Area :
>The Staging Area is when git starts tracking and saving changes that occur in files.
The staging area is a simple file, generally contained in your Git directory,
 that stores information about what will go into your next commit. 

Repository Git:
>where Git stores the metadata and object database for your project. This is the most important part of Git,
and it is what is copied when you clone a repository from another computer.

#### What are remote repositories in git?
>Your repository in ur local computer.

#### Why does a merge conflict occur?
>Deleting lines/Refactoring lines/Bad pushing from colleges
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
>git add filename
#### What does it mean atomic commits and descriptive commit messages?
>Every small steps have to be committed alone, while given a good small 
understandable message to be clear to your colleges/yourself , what is it.
#### What’s the difference between git and GitHub?
>Git is the system/program. Github is a provider to make it better UI/usage to the users.

## Software design

### Clean code

#### What does clean code mean?
> Every function handle a single operation.
> No Global variables.
> Easy to understand variable names.
>Logical Structure.
#### What steps do we usually do during a clean code refactoring?
>Check variable names, spagetthi code refactoring, if we using something more then
2 times , assign it to a single function , and use it.

### Error handling

#### What is exception handling?
>Exception handling is the process of responding to exceptions when a computer program runs.
An exception occurs when an unexpected event happens that requires special processing. 
#### What are the basics of exception handling in Python?
>If we know that a particular section of our program is likely to cause an error,
we can tell Python what to do if it does happen. Instead of letting the error crash our program we can intercept it,
do something about it, and allow the program to continue.

#### In which case should we catch an exception? Why?
>When the program should goes to an error and stop it, or getting wrong input where we have to handle .(register)
#### How can we handle an exception? What can we and should we do with an exception in the ‘except’ block?
> we can handle with try/catch.
#### When do we use an if statement and when exception handling during programming?
>When we can get a foreign input to our program from a different side.
#### What does the else and finally statement in a try-except block in Python?
>When the neither if statement return true, the program will run the else and finally(always run) block.

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?
>To summarize the week , what was bad , what was good, how can we improve from it.

## Programming environment

### Unix

#### What is UNIX and what is Linux?
Unix is propriety kernel designed for a more select audience (ie servers). It is mostly propriety code.

Linux is is designed for a general purpose audience (ie. desktops). It is open source. Linux was based on Unix.
#### What do we call the shell in Linux?
>A Shell provides you with an interface to the Unix system. 
It gathers input from you and executes programs based on that input. When a program finishes executing,
it displays that program's output.

>Shell is an environment in which we can run our commands, programs, and shell scripts.
#### What does root means in a Linux environment?
>root is the user name or account that by default has access to all commands and
files on a Linux or other Unix-like operating system.
It is also referred to as the root account, root user and the superuser.
#### How do you access your hard drives in Linux?
>using the file manager, or a terminal cd.
#### How can you install an application in Linux?
> from terminal ,package manager,be installer files,installing from GUI,
#### What do we call a repository in Linux? (context: package management)
>A Linux repository is a storage location from which your system retrieves and 
installs OS updates and applications. Each repository is a collection of software
hosted on a remote server and intended to be used for installing and updating software packages on Linux systems
#### How do you navigate in the filesystem with the command line?
To navigate into the root directory, use "cd /"
To navigate to your home directory, use "cd" or "cd ~"
To navigate up one directory level, use "cd .."
To navigate to the previous directory (or back), use "cd -"

#### What does the following commands do: mkdir, rm, cat, cp, touch?
- mkdir: Make directory
- rm: Remove files and directories
- cat: Concatenate files and print to stdout.
- cp: Copy files
- touch: Create a new file or update its timestamp.
#### How can you look up what does a command do in Linux if you have no internet connection?
When you use the ip a (or ip addr) command to get information on all the network interfaces on your system
#### What does the following commands do: head, tail, more, less?
- head : displays the first ten lines of a file, unless otherwise stated.
- tail : display the last part of the file
- more : to view a text file one page at a time, press spacebar to go to the next page
- less :  
    - a) You can navigate the page up/down using the less command and not possible in more command.
    - b) You can search a string in less command. (use /keywordto search)
    - c) “more” was fairly limited, and additional development on “more” had stopped
    - d) it uses same functions as vi editor
#### How do you download a file from the internet using the terminal?
- Using wget "http>//example.com/file.zip"
    - wget -P : to download the file to the current directory.
    - wget -O : will download the file to Desktop
    