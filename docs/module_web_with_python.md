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
#### Explain the process of finding the maximum and minimum value in a list of numbers!
#### Explain the process of calculating the average value in an array of numbers!
#### What is Big O complexity? Explain time and space complexity!
#### Explain the process of calculating the average value in a linked list of numbers!

### Procedural
#### How the CASE condition works in SQL?
#### How the switch-case condition works in JavaScript?
#### How to achieve a switch-case-like structure in Python?
#### Explain variable scoping in Python!
#### What’s the difference between const and var in JavaScript?
#### How the list comprehension looks like in Python?
#### How the “ternary expression” looks like in Python?
#### How the ternary expression looks like in JavaScript?
#### How to import a function from another module in Python?
#### How to import a function from another module in JavaScript?

### Functional
#### What is recursion?
#### Write a recursive function which calculates the Fibonacci numbers!
#### How to store a function in a variable in Python?
#### List the ways of defining a callable logical unit in JavaScript!
#### What is an event listener? How to attach one?
#### How to trigger an event in JavaScript?
#### What is a callback function? Tell some examples of its usage.
#### What is a Python decorator? How does it work? Tell some examples of its usage.
#### What is the difference between synchronous and asynchronous execution?

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
#### When do you use the DISTINCT keyword in SQL?
#### What are aggregate functions in SQL? Give 3 examples.
#### What kind of JOIN types do you know in SQL? Could you give examples?
#### What are the constraints in sql?
#### What is a cursor in SQL? Why would you use one?
#### What are database indexes? When to use?
#### What are database transactions? When to use?
#### What kind of database relations do you know? How to define them?
#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?
#### How to include a JavaScript file in a webpage?
#### How to include a CSS file in a webpage?
#### How to select an element using its id in CSS?
#### How to select elements using their class in CSS?
#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?
#### How to select all list items in all ordered lists on the page in CSS?
#### How to select elements using their attributes in CSS?
#### What are UX and UI?
#### Please list some points that an application should fulfill to have good UX.
#### What is XML, XSLT, DTD?
#### What is the difference between HTML and XML?

### Javascript

#### What is javascript?
#### When to use AJAX? Bring examples of its usage.
#### What is DOM and how to manipulate it from Javascript?
#### What are events and how/why to use them in Javascript?
#### What is event bubbling/capturing? How would you use it?
#### What is JSON and how do we use it?

## Software engineering

### Version control

#### What type of branching strategy would you use?
#### What would you do if you find a bug on the production code (master branch)?
#### How can you move changes from one branch to another in GIT?
#### How does a VCS help with code reviews?
#### What is your favorite git command? Why?
#### What does remote/local mean in Git? 

### DevOps

#### Why is it good to use a package manager software?
#### Why is it good to use a virtual environment for a project?

### Networks

#### What kind of HTTP status codes do you know?
#### What is a API?
#### What is REST API?
#### What is JSON? When to use?
#### What is TCP/IP? What layers does it define, what are they responsible for?
#### What’s the difference between TCP and UDP?
#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
#### What is DNS? How does it work?
#### What is a web server?
#### Explain the client-server architecture.
#### What would you use a session for?
#### What would you use a cookie for?

## Software Development Methodologies

#### What kind of software development methodologies do you know? What are the main features of these?
#### What are the SCRUM roles?
#### What are the SCRUM ceremonies?
#### What are the SCRUM artifacts?
#### What is the main goal of a retrospective meeting?
#### Explain, when would you recommend to use the waterfall methodology?
