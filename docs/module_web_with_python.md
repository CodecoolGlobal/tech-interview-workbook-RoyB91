# Web with Python questions

## Software design

### Clean code

#### Point out 5 suggestions, how to format an SQL query!
>Indentation helps keep your query clean by identifying where each block of code begins.
 This makes program structure more understandable.
 
 >Explain Yourself with Comments.
 
 >It is also very important to use a single naming convention for tables, columns, and queries.
  This makes the code easier to write and read.
  
>Define SELECT Fields instead of SELECT *

>Use WHERE instead of HAVING to Define Filters:
>>Per the SQL Order of Operations, HAVING statements are calculated after WHERE statements. 
If the intent is to filter a query based on conditions, a WHERE statement is more efficient.
#### What layers can you name in a simple web application?
    View
    Application service
    Database
    Domain
### Error handling
>Error handling refers to the response and recovery procedures
>from error conditions present in a software application.
>>Error handling helps in maintaining the normal flow of program execution.
#### What error can occur, when an array does not have an element on the requested index?
    IndexError
#### What is the “finally” block, and how would you use it?
>The finally block is as the name implies,
 some code that you want to execute regardless of what happens.
>>A classic example of try…catch…finally is database resource management.    
#### Why should we catch special exception types?
>Nothing is worse than an application crashing with some user unfriendly stacktrace dumped to the screen.
 >>Not only does it give (perhaps unwanted) insight into your code,
     but it also confuses your end-user, and sometimes even scares them away to a competing application.
### Security
#### What is SQL injection? How to protect an application against it?
>An SQL injection is a computer attack in which malicious code is embedded in a poorly-designed application
 and then passed to the backend database
>>You can prevent SQL Injection vulnerabilities in web applications by utilizing parameterized
database queries with bound, typed parameters and careful use of parameterized stored procedures in the database.
>>>Before substitute into query, we need to do the validation. for remove ir escaped the special character like single quote, key words like select, Union…
>>>>Don’t use normal query, use Named query like this

#### What is XSS? How to protect an application against it?
    Cross-site Scripting (XSS)
>Cross-site Scripting (XSS) is a client-side code injection attack. The attacker aims to execute malicious scripts in a web browser of the victim
by including malicious code in a legitimate web page or web application.
>>commonly used for Cross-site Scripting attacks are forums, message boards, and web pages that allow comments.
    
    To protect:
>To protect against stored XSS attacks, make sure any dynamic content coming from the data store cannot be used
 to inject JavaScript on a page.
 >> - Whitelist Values
 
 >> - HTTP-only Cookies : meaning that cookies will be received, stored, and sent by the browser, but cannot be modified or read by JavaScript.
 
 >> - disallow the characters – especially < and > characters – from being rendered
#### How to properly store passwords?
>First of all you have to hash the password and store data information like that in the database.
>>Secondly you need a good encrypt algorithm for that process.
>>>Finally the best practise the you storing your database a specific local storage.(etc.)
#### What is HTTPS?
>Hypertext Transfer Protocol Secure (HTTPS) is an extension of the Hypertext Transfer Protocol (HTTP).
 It is used for secure communication over a computer network, and is widely used on the Internet
>>It protects against man-in-the-middle attacks. 
#### What is encryption and decryption?
>Encryption is the process of translating plain text data (plaintext) into something that appears to be random and meaningless (ciphertext).
 >>Decryption is the process of converting ciphertext back to plaintext.
#### What is hashing?
>A hash function is where a computer takes an input of any length and content (e.g. letters, numbers, and symbols) and
 uses a mathematical formula to chop it, mix it up, and produce an output of a specific length. 
#### What is the difference between encryption and hashing? When would you use which?
>The key difference between encryption and hashing is that encrypted strings can be reversed back into their original
 decrypted form if you have the right key.
 
    Hashing:
    Hashing is an ideal way to store passwords,
    as hashes are inherently one-way in their nature.
    + salt
    
    Encryption:
    Encryption should only ever be used over hashing when
     it is a necessity to decrypt the resulting message.
     for example: send a secure messages to someone on the other side of the world 
#### What encryption methods do you know?
    RSA:
    RSA is considered an asymmetric algorithm due to its use of a pair of keys.
    You’ve got your public key,which is what we use to encrypt our message,
     and a private key to decrypt it
#### What hashing methods do you know?
    MD5(its already broken,easy to manipulate) , SHA-2(Secure Hash Algorithm),
#### How/where would you store sensitive data (like db password, API key, ...) of your application?
>Of course i would encrypt it, or hash it first.

>After that:
>>I would rent a local storage(there are lot of companies who are offering local servers for these priceless information)
 ,or if my company big enough build one.
## Computer science

### Algorithms

#### What is the difference between Stack and Queue data structure?
|  STACKS | QUEUES  |
|---|---|
| Stacks are based on the LIFO principle, i.e., the element inserted at the last, is the first element to come out of the list.  | Queues are based on the FIFO principle, i.e., the element inserted at the first, is the first element to come out of the list.  |
| Insert operation is called push operation.  | Insert operation is called enqueue operation.
| Delete operation is called pop operation.  |  Delete operation is called dequeue operation. |
| In stacks we maintain only one pointer to access the list, called the top(last element)  | In queues we maintain two pointers to access the list(first/last position  |
#### What is BubbleSort? Describe the main logic of this sorting algorithm.
>Bubble Sort is a sorting algorithm that works by repeatedly
swapping the adjacent elements if they are in wrong order.(it compare each pair of adjacent elements of the list )
#### Explain the process of finding the maximum and minimum value in a list of numbers!
>If array is sorted, that's the best you're going to get. If it is sorted,
 just take the first and last elements.
#### Explain the process of calculating the average value in an array of numbers!
>The sum of the numbers(of the array) divided by the number of values.
#### What is Big O complexity? Explain time and space complexity!
>Big O Notation is the language we use for talking about how long an algorithm takes to run.
 It is how we compare the efficiency of different approaches to a problem.
- how quickly the runtime grows : use Big O Notation to talk about how quickly the runtime grows.

- relative to the input :  With Big O Notation, we use the size of the input, which we call “n”. So we can say things like the runtime grows “on the order of the size of the input” (O(n))
 or “on the order of the square of the size of the input” (O(n²)).


- as the input gets larger : we care more about the stuff that grows fastest as the input grows,
 because everything else is quickly eclipsed as n gets very large.
#### Explain the process of calculating the average value in a linked list of numbers!

    sum all of the data values and divide by the number of nodes in the list.

### Procedural

#### How the CASE condition works in SQL?
>The CASE statement goes through conditions and returns a value when the first condition is met.

>>So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.
#### How the switch-case condition works in JavaScript?
>The switch statement is used to perform different actions based on different conditions.

>>Use the switch statement to select one of many code blocks to be executed.

#### How to achieve a switch-case-like structure in Python?
>The Pythonic way to implement switch statement is to use the powerful dictionary mappings, also known as associative arrays,
 that provide simple one-to-one key-value mappings.
 ````python
def switch_demo(argument):
    switcher = {
        1: "January",
        2: "February",
        3: "March",
        4: "April",
        5: "May",
        6: "June",
        7: "July",
        8: "August",
        9: "September",
        10: "October",
        11: "November",
        12: "December"
    }
    print(switcher.get(argument, "Invalid month")) # Invalid month is default if number not found
 ````
#### Explain variable scoping in Python!
    LEGB Rule.

    L, Local — Names assigned in any way within a function (def or lambda)),
    and not declared global in that function.
    
    E, Enclosing-function locals — Name in the local scope of any and
    all statically enclosing functions (def or lambda), from inner to outer.
    
    G, Global (module) — Names assigned at the top-level of a module file,
    or by executing a global statement in a def within the file.
    
    B, Built-in (Python) — Names preassigned in the built-in names module : open,range,SyntaxError,...
    
    example:
```python
code1
class Foo:
   code2
   def spam.....
      code3
      for code4..:
       code5
       x()
```
    The for loop does not have its own namespace. In LEGB order, the scopes would be
    
    L : local, in def spam (in code3, code 4, code5).
    
    E : Enclosed function, any enclosing functions (if the whole example were in another def)
    
    G : Global. Were there any x declared globally in the module (code1)?
    
    B : Any builtin x in Python.
    
    x will never be found in code2
#### What’s the difference between const and var in JavaScript?
>The const keyword creates a declaration that cannot be reassigned.
WHERE u can reassign with var(+var is global scoped)
#### How the list comprehension looks like in Python?
```python
# You can either use loops:
squares = []

for x in range(10):
    squares.append(x**2)
 
print(squares)
#result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Or you can use list comprehensions to get the same result:
squares = [x**2 for x in range(10)]

print(squares)
#result: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]     
```
#### How the “ternary expression” looks like in Python?
```python
a = val_if_true if test else val_if_false
```
    in action:
```python
d = {'a': 'x', 'b': 'y', 'c': 'x'}

def has_unique_value(k):
    return d.values().count(d[k]) == 1

def keys_with_same_value_as_key(k):
    return set([key for key in d.keys() if d[key] == d[k]])

print( {d[k]:k if has_unique_value(k) else keys_with_same_value_as_key(k) for k in d.keys()} )
```
#### How the ternary expression looks like in JavaScript?
    with if/else:
```javascript
if (person.age >= 16) {
  person.driver = 'Yes';
} else {
  person.driver = 'No';
}
```
    with tenary expression:
```javascript
person.driver = person.age >=16 ? 'Yes' : 'No';
```
#### How to import a function from another module in Python?
```python
    from a import b, c
```
#### How to import a function from another module in JavaScript?
```javascript
    import "my-module.js";
    import myModule from "my-module.js";
    import {reallyReallyLongModuleMemberName as shortName} from "my-module.js";
```

### Functional
#### What is recursion?
>In the recursive program, the solution to the base case is provided and the solution
 of the bigger problem is expressed in terms of smaller problems.
#### Write a recursive function which calculates the Fibonacci numbers!
```python
def function(number):
  if number == 0:
    return 0
  if number == 1:
    return 1
  else:
    return function(number-1) + function(number-2)
```
#### How to store a function in a variable in Python?
```python
def one():
    print("hello from function one")

function_variable = one

print(function_variable)
```
#### List the ways of defining a callable logical unit in JavaScript!
- arrow function
```javascript
    const foo = (arg1, arg2) => {
        ...
    };
```
- concise method syntax:
```javascript
    let obj = {
        myMethod(arg1, arg2) {
            ...
        }
    };
```
#### What is an event listener? How to attach one?
>It sets up a function that will be called whenever the specified event is delivered to the target. 
```javascript
document.getElementById("myBtn").addEventListener("click", displayDate);
```
#### How to trigger an event in JavaScript?
>To create the event you want to fire, you can use either createEvent
 or createEventObject depending on the browser.
#### What is a callback function? Tell some examples of its usage.
> A callback is a function that is to be executed after another function has finished executing —
hence the name ‘call back’.
>>More complexly put: In JavaScript, functions are objects. Because of this, functions can take functions as arguments,
 and can be returned by other functions.
 ```javascript
function doHomework(subject, callback) {
  alert(`Starting my ${subject} homework.`);
  callback();
}
function alertFinished(){
  alert('Finished my homework');
}
doHomework('math', alertFinished);
```
>>As you can see, we’ve passed the alertFinished function definition as an argument during our doHomework() function call!
#### What is a Python decorator? How does it work? Tell some examples of its usage.
>>A decorator takes in a function, adds some functionality and returns it.
```python
def smart_divide(func):
   def inner(a,b):
      print("I am going to divide",a,"and",b)
      if b == 0:
         print("Whoops! cannot divide")
         return

      return func(a,b)
   return inner

@smart_divide
def divide(a,b):
    return a/b
```
#### What is the difference between synchronous and asynchronous execution?
>>When you execute something synchronously, you wait for it to finish before moving on to another task. When you execute something asynchronously,
 you can move on to another task before it finishes.


>Synchronous execution means the execution happens in a single series.  
- A->B->C->D. 
>If you are calling those routines, A will run, then finish, then B will start, then finish, then C will start, etc.


>With Asynchronous execution, you begin a routine, and let it run in the background while
you start your next, then at some point, say "wait for this to finish". It's more like:
>- Start A->B->C->D->Wait for A to finish

>The advantage is that you can execute B, C, and or D while A is still running 
(in the background, on a separate thread), so you can take better advantage
 of your resources and have fewer "hangs" or "waits".

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
>Everything On One Server

- The entire environment resides on a single server. For a typical web application,
 that would include the web server, application server, and database server
>Separate Database Server

- The database management system (DBMS) can be separated from the rest of the environment to eliminate the resource
 contention between the application and the database, and to increase security

#### When do you use the DISTINCT keyword in SQL?
> When u don't want a duplicate in a query.
#### What are aggregate functions in SQL? Give 3 examples.
    An aggregate function allows you to perform a calculation
    on a set of values to return a single scalar value.
        - AVG – calculates the average of a set of values.
        - COUNT – counts rows in a specified table or view.
        - MIN
        - MAX
        - SUM
#### What kind of JOIN types do you know in SQL? Could you give examples?
    Inner Join:(returns records at the intersection of the two tables.)
```postgresql
select first_name, last_name, order_date, order_amount
from customers c
inner join orders o
on c.customer_id = o.customer_id
```
    Left Join:(A left join returns all records from table A and any matching records from table B.)
```postgresql

select first_name, last_name, order_date, order_amount
from customers c
left join orders o
on c.customer_id = o.customer_id
```
    Right Join:(Right join is a mirror version of the left join and allows to get a list of all orders, appended with customer information.)
    
    Full Join:(Finally, for a list of all records from both tables, we can use a full join.)
#### What are the constraints in sql?
>>SQL constraints are used to specify rules for data in a table.

- NOT NULL - Ensures that a column cannot have a NULL value
- UNIQUE - Ensures that all values in a column are different
- PRIMARY KEY - A combination of a NOT NULL and UNIQUE. Uniquely identifies each row in a table
- FOREIGN KEY - Uniquely identifies a row/record in another table
#### What is a cursor in SQL? Why would you use one?
>A cursor is a temporary work area created in the system memory when a SQL statement is executed. A cursor contains information on a select statement and the rows of data accessed by it.
This temporary work area is used to store the data retrieved from the database, and manipulate this data. A cursor can hold more than one row, but can process only one row at a time. The set of rows the cursor holds is called the active set.
#### What are database indexes? When to use?
>A database index is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional writes and storage space to maintain the index data structure.
Indexes are used to quickly locate data without having to search every row in a database table
#### What are database transactions? When to use?
>A transaction is a unit of work that you want to treat as "a whole." It has to either happen in full or not at all.

>A classical example is transferring money from one bank account to another. To do that you have first to withdraw the amount from the source account, and then deposit it to the destination account. The operation has to succeed in full. If you stop halfway, the money will be lost, and that is Very Bad.

>In modern databases transactions also do some other things - like ensure that you can't access data that another person has written halfway. But the basic idea is the same - transactions are there to ensure, that no matter what happens, the data you work with will be in a sensible state. They guarantee that there will NOT be a situation where money is withdrawn from one account, but not deposited to another.


#### What kind of database relations do you know? How to define them?
    One-to-One:
    
    A row in table A can have only one matching row in table B, and vice versa.



    One-to-Many (or Many-to-One):
    
    This is the most common relationship type. In this type of relationship,
    a row in table A can have many matching rows in table B,
    but a row in table B can have only one matching row in table A.
    (Each customer can only be assigned one city,. One city can be assigned to many customers.)
    
   
    
    Many-to-Many
    
    A many-to-many relationship could be thought of as two one-to-many relationships,
    linked by an intermediary table( “cross-reference table”).
    (So in order to create a many-to-many relationship between the Customers table and the Products table,
    we created a new table called Orders.)
           
#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
```postgresql
select * table
where address like "%Miskolc%"
```
#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?
>I would create a person_log table and create a trigger on  that will insert a row into person_log table
 whenever the table/s row/s get updated/deletes/added

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?
    - Both are markup languages, which represents text data in proper format using tags. However they are used for completely different purposes.

    Similarities between HTML and XML?
     1. Both are languages of web.
     2. Both are markup languages.
     3. Both are originated from SGML. [Standardized General Markup Language]
     4. Tags are basic building blocks of both HTML and XML documents.
     
     Differences between HTML and XML
     1. HTML tags are predefined tags where as XML tags are user defined tags.
     2. HTML tags are limited number of tags where as XML tags are extensible.
     3. HTML tags are case insensitive where as XML tags are sensitive.
     4. HTML tags are meant for displaying the data but not for describing the data where as XML tags are meant for describing the data.
     5. HTML focuses on how data looks where as XML focuses on what data is.

    XHTML:
    1. XHTML stands for EXtensible HyperText Markup Language
    2. XHTML is almost identical to HTML
    3. XHTML is stricter than HTML
    4. XHTML is HTML defined as an XML application
        
    
#### How to include a JavaScript file in a webpage?
> In .html file we use the script tag to import it. :
```html
<script type="text/javascript" src="path-to-javascript-file.js"></script>
```
#### How to include a CSS file in a webpage?
>Using the link tag in .html file
```html
<link rel="stylesheet" type="text/css" href="stylesheet.css"/>
```
#### How to select an element using its id in CSS?
> You have to use the hashtag(#) + the element id name:
```css
#elementIdName {
    /*code;*/
}
```
#### How to select elements using their class in CSS?
>You have to use the dot(.) + element class name:
```css
.classname {
    /*code;*/
}
```
#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?
> You have to define in css file with dot classname dot classname :
```css
.alpha.beta{color:red;}
/*here you can reach the beta class*/
```
#### How to select all list items in all ordered lists on the page in CSS?
> You can reach by using the ordered tag which is < ol >:
```css
ol {
 /*code;*/
}
```
#### How to select elements using their attributes in CSS?
```css
/*We can reach differently*/

[data-value] {
  /* Attribute exists */
}

[data-value="foo"] {
  /* Attribute has this exact value */
}

[data-value*="foo"] {
  /* Attribute value contains this value somewhere in it */
}

[data-value~="foo"] {
  /* Attribute has this value in a space-separated list somewhere */
}

[data-value^="foo"] {
  /* Attribute value starts with this */
}

[data-value|="foo"] {
  /* Attribute value starts with this in a dash-separated list */
}

[data-value$="foo"] {
  /* Attribute value ends with this */
}
```
#### What are UX and UI?
>UI:
>>The “UI” in UI design stands for “user interface.” The user interface is the graphical layout of an application.
It consists of the buttons users click on, the text they read, the images, sliders, text entry fields, and all the rest of the items the user interacts with. This includes screen layout, transitions,
interface animations and every single micro-interaction. Any sort of visual element, interaction, or animation must all be designed.

>UX:
>>“UX” stands for “user experience.” A user’s experience of the app is determined by how they interact with it.
User experience is determined by how easy or difficult it is to interact with the user interface elements that the UI designers have created.
#### Please list some points that an application should fulfill to have good UX.
    -useful : Your content should be original and fulfill a need
    -usable : Site must be easy to use
    -valuable 
    -accesible : Content needs to be accessible to people with disabilities (example:colorblind)
    -desirable: evoke emotion and appreciation
#### What is XML, XSLT, DTD?
>First we will start at the top. The VERY top. SGML stands for Standard Generalized Markup Language. Simply put, it is the very root coding of coding. HTML is an application of SGML. 

- XML is a simplified subset of SGML. It stands for eXtensible Markup Language. 

- DTD stands for Document Type Declaration. It is a set of instructions that states what tags are usable and what (re)action they create. Each browser has a DTD set in it's programming set by the browser companies. This is how some tags will work in only one type of browser or version. It has the tags stated in it's DTD. XML makes it possible to create unique tag sets by applying it's own DTD. This makes the DTD more compatable with more browsers. 

- XSLT stands for eXtensible Stylesheet Language Transformation. It is a strong verions of CSS that formats the XML page for viewing.
#### What is the difference between HTML and XML?
     Differences between HTML and XML
     1. HTML tags are predefined tags where as XML tags are user defined tags.
     2. HTML tags are limited number of tags where as XML tags are extensible.
     3. HTML tags are case insensitive where as XML tags are sensitive.
     4. HTML tags are meant for displaying the data but not for describing the data where as XML tags are meant for describing the data.
     5. HTML focuses on how data looks where as XML focuses on what data is.

### Javascript

#### What is javascript?
    JavaScript is the Programming Language for the Web
    - can update and change both HTML and CSS
    - can calculate, manipulate and validate data
#### When to use AJAX? Bring examples of its usage.
>Ajax programming is that you can exchange data in the background without actually disturbing the user experience.
>>And when you want render the access of data more efficiently and effectively.
    
    Things That Are Good for Ajax:
        - Form validation : ( It's so much nicer when the form tells
            you as you are typing if you've filled it out wrong or not. )
        
        - Comments: (when a commenter hits the comment button, it's nice to see the comment appear immediately on the page.)
        
        - Login Forms
        - Auto-Complete(when searching for example)
        - Voting and Rating (forums)
        - Updating With User Content
        - Chat Rooms And Instant Messaging
        - Lightboxes instead of pop-ups
#### What is DOM and how to manipulate it from Javascript?
> When a web page is loaded, the browser creates a Document Object Model of the page.(DOM)
>>You can manipulate DOM via .js file which is imported to your html file with a < script > tag.
```javascript
let element = document.querySelector('selector')

/* You can use it to get the element from the DOM and save
it as a variable, and manipulate it.  */


let btn = document.querySelector('button');
btn.addEventListener('click', foo);

/*Or give it a event listener for a specific  element*/


let pEle = document.createElement('p')

/*You can even create elements*/


let div = document.querySelector('div');
div.setAttribute('contentEditable', '')
/* method either adds a new attribute to an HTML element, or updates the value*/
```
#### What are events and how/why to use them in Javascript?
Events occur when the page loads, when user interacts (clicks, hovers, changes) and myriad other times, and can be triggered manually too.

How:
>The addEventListener method is the most preferred way to add an event listener to window, document or any other element in the DOM.
```javascript
let btn = document.querySelector('button');
btn.addEventListener('click',function(event) {
  }
);
```
Why:
>Because ,JavaScript in the browser uses an event-driven programming model.
```! Everything starts by following an event !```


#### What is event bubbling/capturing? How would you use it?
Event bubbling and capturing are two ways of event propagation in the HTML DOM API,
when an event occurs in an element inside another element,
and both elements have registered a handle for that event.

When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors.

With ````capturing````, the event is ````first```` captured by the ````outermost element```` and propagated ```to the inner elements```.

Event capturing:

When you use event capturing

               
    ---------------| |-----------------
    | element1     | |                |
    |   -----------| |-----------     |
    |   |element2  \ /          |     |
    |   -------------------------     |
    |        Event CAPTURING          |
    -----------------------------------
the event handler of element1 fires first, the event handler of element2 fires last.

Event bubbling:

When you use event bubbling
    
                   / \
    ---------------| |-----------------
    | element1     | |                |
    |   -----------| |-----------     |
    |   |element2  | |          |     |
    |   -------------------------     |
    |        Event BUBBLING           |
    -----------------------------------
the event handler of element2 fires first, the event handler of element1 fires last.
#### What is JSON and how do we use it?
- JSON is short for JavaScript Object Notation, and is a way to store information in an organized, easy-to-access manner.
 In a nutshell, it gives us a human-readable collection of data that we can access in a really logical manner.
```JSON (in Javascript) is a string!```

How to use it:
- In short, you are forced to communicate things using key-value pairs and arrays.
- JSON is basically a way of communicating data to someone, with very, very specific rules.

## Software engineering

### Version control

#### What type of branching strategy would you use?
I would use the GitHub Flow:

    - Code in master is deployable at all times.
    - When you want to start working on a new task, create a new branch off of master and give it a descriptive name.
    - Commit to that branch locally and regularly send your work to the same-named branch on the server.
    - Open a pull request when you feel your changes are ready to be merged (or even if you aren’t so sure, but would like some feedback).
    - After the new feature is revised and approved, you can merge it into master.
    - Once your changes are merged and pushed to the master, you can and should delete the branch.
    
#### What would you do if you find a bug on the production code (master branch)?
I would report it to my project manager. And he/she would tell us how/who should fix it.
#### How can you move changes from one branch to another in GIT?
```git
git branch checkout branchname
```
#### How does a VCS help with code reviews?
- Modern version control systems are designed to help address problems that teams face when collaborating.
- Breaking down silos and embracing more perspectives and conversations can enable you and your team to deliver better software. 

#### What is your favorite git command? Why?
```git
git push 
```
>It means i developed something which is working(function) in the project.

#### What does remote/local mean in Git? 
- A remote in Git is a common repository that all team members use to exchange their changes.
- Git local repository is the one on which we will make local changes, typically this local repository is on our computer.

### DevOps

#### Why is it good to use a package manager software?
- They prevent mixing incompatible files/libraries. 

- They establish a shared convention for managing libraries.(When new developers come onto your project, team, company, etc., they're likely to know the conventions of the package manager.
This means they don't have to waste time figuring out the fine details of how libraries are managed in your code base.)

- They give you a standard way of versioning and distributing your own dependencies and files that don't belong in your repository.

- Some package managers provide additional features during installation. 

- They tend to centralize hosting and distribution. 

- Helps with complex dependency trees (and that can be managed downloading a dependency together with all its dependencies).

- Packages contain metadata, such as the software's name, description of its purpose, version number, vendor, checksum,
 and a list of dependencies necessary for the software to run properly
 
 
#### Why is it good to use a virtual environment for a project?
- Dependency Management: Prevent conflicts between dependencies of multiple projects.
- Every project can have a single unique virtual environment with the specific packages. 
### Networks

#### What kind of HTTP status codes do you know?
- 200   OK             
- 301   Moved Permanently
- 302   Found
- 400   Bad Request
- 403   Forbidden 
- 404   Not Found 
- 405   Method Not Allowed
- 408   Request Timeout
- 500   Internal Server Error
- 504   Gateway Timeout

#### What is a API?
- API stands for Application Programming Interface.
   - An API, or application programming interface, is essentially a way for apps to borrow functionality and data from each other.
- An API is code, that allows two software programs to communicate with each other. One program can call another programs API to get access to data or functionality of the other program.
- An API is the messenger that takes a request, tells a system what you want to do and then returns the response back to you!
#### What is REST API?
- A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data.
#### What is JSON? When to use?
- JSON is short for JavaScript Object Notation, and is a way to store information in an organized, easy-to-access manner.
 In a nutshell, it gives us a human-readable collection of data that we can access in a really logical manner.
 - ```JSON (in Javascript) is a string!```


When to use it:
- In short, you are forced to communicate things using key-value pairs and arrays.
- for fast and and effective communication between server -user for example.
#### What is TCP/IP? What layers does it define, what are they responsible for?
- Transmission Control Protocol/Internet Protocol (TCP/IP) is the language a computer uses to access the internet.
 It consists of a suite of protocols designed to establish a network of networks to provide a host with access to the internet.
(its like a set of rules to allow communicate each other)

    
**Layer**|**Primary function**|**Examples**
:-----:|:-----:|:-----:
Application|Do useful work|HTTP, SMTP, POP, Ping, FTP
Transport|Control the flow of information between the application program running on the client and the application program running on the server|TCP (reliable), UDP (not reliable)
Network|Route packets between networks (inter-network)|IP
Data link|Move data within a local area network|Ethernet, ATM, PPP
Physical|Define the physical characteristics of the communication hardware and medium|radio, twisted pair, fiber

#### What’s the difference between TCP and UDP?
>TCP (Transmission Control Protocol) is connection oriented, whereas UDP (User Datagram Protocol) is connection-less. This means that TCP tracks all data sent, requiring acknowledgment for each octet (generally). UDP does not use acknowledgments at all, and is usually used for protocols where a few lost datagrams do not matter.

**TCP**|**UDP**
:-----:|:-----:
Reliable|Unreliable
Connection-oriented|Connectionless
Segment retransmission and flow control through windowing|No windowing or retransmission
Segment sequencing|No sequencing
Acknowledge sequencing|No acknowledgment  

  
#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
A simple request message from a client computer consists of the following components:

- A request line to get a required resource, for example a request GET /content/page1.html is requesting a resource called /content/page1.html from the server.
- Headers (Example – Accept-Language: EN).
- An empty line.
- A message body which is optional.
- All the lines should end with a carriage return and line feed. The empty line should only contains carriage return and line feed without any spaces.

#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
A simple response from the server contains the following components:

- HTTP Status Code (For example HTTP/1.1 301 Moved Permanently, means the requested resource was permanently moved and redirecting to some other resource).
- Headers (Example – Content-Type: html)
- An empty line.
- A message body which is optional.
#### What is DNS? How does it work?
Domain Name Servers (DNS) are the Internet's equivalent of a phone book.
They maintain a directory of domain names and translate them to Internet Protocol (IP) addresses.
#### What is a web server?
A Web server is a program that uses HTTP (Hypertext Transfer Protocol) to serve the files that form Web pages to users, in response to their requests, which are forwarded by their computers' HTTP clients.
Dedicated computers and appliances may be referred to as Web servers as well.
#### Explain the client-server architecture.
Client-server architecture, architecture of a computer network in which many clients (remote processors) request and
receive service from a centralized server (host computer).
>Client computers provide an interface to allow a computer user to request services of the server and to display the results the server returns. 
#### What would you use a session for?
The ````purpose for session```` is to store data that you (as the web application developer)
```would like to have preserved across page loads```. Thus, you can set flags in your login script
such as logged_in to check if the user is logged in, and on any
other page check session['logged_in'] == true, instead of querying for that information.
- Sessions use a cookie as a key of sorts, to associate with the data that is stored on the server side.
- IDU is stored on server (i.e. server-side)
- Safer (because of 1)
- Expiration can not be set, session variables will be expired when users close the browser. 

#### What would you use a cookie for?
 You can save settings to cookie for the websites between visits.So its gonna remember your previous preferences.
Cookies:

- IDU is stored on web-browser (i.e. client-side)
- Not very safe, since hackers can reach and get your information (because of 1)
- Expiration can be set (see setcookies() for more information)
## Software Development Methodologies

#### What kind of software development methodologies do you know? What are the main features of these?
Waterfall development methodology:
 
    - requierements -> Desing -> Implementation -> Verification -> Maintanance 
>It’s a rigid linear model that consists of sequential phases
(requirements, design, implementation, verification, maintenance) in which distinct goals are accomplished. 
Each phase must be 100% complete before the next phase can start,
and traditionally there is no process for going back to modify the project or direction. 

Agile development methodology:
    ![image](https://www.visual-paradigm.com/servlet/editor-content/scrum/what-are-scrum-ceremonies/sites/7/2018/11/the-agile-scrum-framework.png)
 
     -> Requirement/Features/User stories/Product Backlog ->
     -> Scrum Team(with lead) ->
     -> Sprint Planning(relative time)->
     -> Sprints 1-4 Weeks Duration -> 
     -> Production deployment ->
     -> Done Checklist
     (While this process other people making the desing,build it,inegrate,test the software) - >
     -> Sprint Retrospective ->
     -> Product review(customer input)->
     -> Potential Product Increment
     
#### What are the SCRUM roles?
- One of the most important things for the success of scrum is the role of the ```Product Owner```,
 who serves as an interface between the team and other involved parties (stakeholders).
 
 - The ```Scrum Master``` does not interfere into the decisions of the team regarding specifically the development,
 but rather is there for the team as an advisor. He ````only interferes```` actively ```when anybody```
 of the team or any other participant of a project (Stakeholder) ````does not obey the rules of Scrum.```` 

- The ````Development Team```` in Scrum a team is not just the executive organ that receives its tasks from the project leader, it rather decides self dependent,
 which requirements or User Stories it can accomplish in one sprint. 
#### What are the SCRUM ceremonies?
*Ceremonies*|
:-----:|
Sprint Planning|
Sprint review|
Sprint retrospective|
Daily Scrum|

#### What are the SCRUM artifacts?
*Artifacts*|
:-----:|
Increment|
Product backlog|
Sprint backlog|

#### What is the main goal of a retrospective meeting?
This is where the Scrum Team meets ```to reflect on their previous Sprint``` and to figure out ````how to improve as a team```` by asking – what went well,
what did not and what can be improved. ```It allows``` the team to focus on its ```overall performance``` and identify strategies for continuous ````improvement.````
#### Explain, when would you recommend to use the waterfall methodology?
Use Waterfall when:

- the project is simple
- the project is complicated, but you have the expertise to deliver it
- it is all you know and you have no support for change
- the upfront investment is not risky to make
- you focus your performance measures on delivery date and budget
