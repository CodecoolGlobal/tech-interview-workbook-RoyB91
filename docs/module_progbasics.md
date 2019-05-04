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
#### What do we call an *in-place* sort?
### Programming paradigms - procedural

#### What is “Stack overflow”? Write a code, that ends up with stack overflow. What is the call stack?
#### What is the function signature?

### Programming languages - Python
#### How do you use a dictionary in Python?
#### What does it mean that an object is Immutable in Python?
#### What is conditional expression in Python?
#### What are different types of arguments in Python?
#### What is variable shadowing? (context: variable scope)
#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it in Python?
#### What happens if you try to add an item to the end of a List, while you are iterating over it in Python?
#### What is the "golden rule" of variable scoping in Python? What is the lifetime of variables?
#### If you need to access the iterator variable after a for loop, how would you do it in Python?
#### What type of elements can a list contain in Python?
#### What is slicing in Python?
#### What arithmetic operators (+,*,-,/) can be used on lists in Python? What do they do?
#### What is the purpose of the in and not in membership operators in Python?
#### What does the + operator mean when used with strings in Python?
#### How do you format strings in Python with the format() function?
#### Name 4 iterable types in Python!
#### What is the difference between list, set, dictionary comprehension and a generator expression in Python?
#### Does the order of the function definitions matter in Python? Why?
#### What is the difference between input parameters and local variables in Python?
#### What does unpacking mean in Python?
#### What happens when you try to assign the result of a function which has no return statement to a variable in Python?
#### What is the difference between positional and keyword parameters in Python?

## Software engineering

### Debugging

#### What techniques can you use while debugging a program in Python?
#### What does step over, step into and step out mean while using the debugger?
#### How can you start the program from a certain line using the debugger? (careful, tricky! :) )

### Version control

#### What are the advantages of using a version control system?
#### What is the difference between the working directory, the staging area and the repository in git?
#### What are remote repositories in git?
#### Why does a merge conflict occur?
#### Through what series of commands could you put a new file into a remote repository connected to your existing local repository?
#### What does it mean atomic commits and descriptive commit messages?
#### What’s the difference between git and GitHub?

## Software design

### Clean code

#### What does clean code mean?
#### What steps do we usually do during a clean code refactoring?

### Error handling

#### What is exception handling?
#### What are the basics of exception handling in Python?
#### In which case should we catch an exception? Why?
#### How can we handle an exception? What can we and should we do with an exception in the ‘except’ block?
#### When do we use an if statement and when exception handling during programming?
#### What does the else and finally statement in a try-except block in Python?

## Software Development Methodologies

#### What is the main goal of a retrospective meeting?

## Programming environment

### Unix

#### What is UNIX and what is Linux?
#### What do we call the shell in Linux?
#### What does root means in a Linux environment?
#### How do you access your hard drives in Linux?
#### How can you install an application in Linux?
#### What do we call a repository in Linux? (context: package management)
#### How do you navigate in the filesystem with the command line?
#### What does the following commands do: mkdir, rm, cat, cp, touch?
#### How can you look up what does a command do in Linux if you have no internet connection?
#### What does the following commands do: head, tail, more, less?
#### How do you download a file from the internet using the terminal?
