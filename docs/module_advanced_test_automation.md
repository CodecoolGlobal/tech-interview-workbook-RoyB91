# Test automation questions

### Testing Basics (ISTQB related)

#### What is the purpose of testing? What is not?
    Testing verifies that the system meets the different requirements including,
    functional, performance, reliability, security, usability and so on.
    This verification is done to ensure that we are building the system right.
  
    
   -    **What is not**:
        -    to ensure the software is not a good product
        -    to blame the developers who wrote the code(communication)
             
#### What is the difference between Defect, Error, Failure?
-   **Defect**:
     It can be simply defined as a variance between expected and actual.
     Defect is an error found AFTER the application goes into production.
     It commonly refers to several troubles with the software products,
     with its external behavior or with its internal features.

-   **Error**:
    An error is a mistake, misconception, or misunderstanding on the part of a software developer.
    In the category of developer we include software engineers, programmers, analysts, and testers. 
   
-   **Failure**:
    A failure is the inability of a software system or component to perform its required functions within specified performance requirements.
    When a defect reaches the end customer it is called a Failure.

#### What are the testing principles?
-   **Testing shows the presence of defects, not their absence**:
    -   Testing can show that defects are present, but cannot prove that there are no defects.  

-   **Exhaustive testing is impossible**:
    -   Testing everything is not possible except for trivial cases.
    -   Rather than attempting to test exhaustively, risk analysis, test techniques, and priorities should be used to
        focus test efforts.
        
-   **Early testing saves time and money**:
    -   To find defects early, both static and dynamic test activities should be started as early as possible in the
        software development lifecycle.

-   **Defects cluster together**:
    -   Predicted defect clusters, and the actual observed
        defect clusters in test or operation, are an important input
        into a risk analysis used to focus the test effort.
  
  - **Beware of the pesticide paradox**:
    -   To detect new defects, existing tests and test data may need changing, and new tests may need to be
        written.
    -   In some cases, such as automated regression testing, the pesticide paradox has a
        beneficial outcome.
  
  - **Testing is context dependent**:
    -   Testing is done differently in different contexts.
    
  - **Absence-of-errors is a fallacy**:
    -   Overall important to give a customer what he/she wants , a working products.(not mayor bugs,etc.)

#### What is unit testing? Who is responsible to write unit tests?
Unit testing where **developer** test his/her own block of code(method,function)

#### What are Test Levels, what is the difference between them?
**Component Testing**:
-   Component testing (also known as unit or module testing) focuses on components that are separately
    testable.

**Integration Testing**:
-   Integration testing focuses on interactions between components or systems. Objectives of integration
    testing include.

**System Testing**:
-   System testing focuses on the behavior and capabilities of a whole system or product, often considering
    the end-to-end tasks the system can perform and the non-functional behaviors it exhibits while performing
    those tasks.
    
**Acceptance Testing**:
-   Acceptance testing, like system testing, typically focuses on the behavior and capabilities of a whole
    system or product.
    -   Establishing confidence in the quality of the system as a whole.
    -   Validating that the system is complete and will work as expected.
    -   Verifying that functional and non-functional behaviors of the system are as specified.
    
    
#### What is the difference between verification and validation?
**verification**:
-   To verify whether all specified requirements have been fulfilled.

**validation**:
-   To validate whether the test object is complete and works as the users and other stakeholders
    expect.
    
    
#### What are Testing Types, what is the difference between them?
**Functional Testing**:
-   what the system should do.

**Non-functional testing**:
-   how the system should work.
#### What is the difference between white box, grey box and black box testing?
-   In White Box testing internal structure (code) is known.

-   In Black Box testing internal structure (code) is unknown.

-   In Grey Box Testing internal structure (code) is partially known.
#### What is the difference between UAT (User Acceptance Testing) and System testing?
**UAT**:
-   has a somewhat broader scope that focuses the user-facing aspects of the software product.

**SIT**:
-   zooms in on the interoperation of the subsystems (software and hardware) constituting the product.
    SIT is more detailed, and it strives for a complete functional coverage of the system.
#### Mention the differences between Regression Testing, Smoke Testing and Retesting?
**Smoke Testing**:
-    We do smoke test whenever we receive a new build that is relative unstable to ensure that
the critical functionalities of the AUT working fine.

**Retesting**:
-   We do retesting for a feature/function which had defects (bugs) & those bugs have been fixed recently.

**Regression testing**:
-   Regression testing involves running tests to detect such unexpected side-effects of the product.

#### What is risk-based testing, whats the point of it?
-   Risk is used to focus the effort required during testing. It is used to decide where and when to start testing
and to identify areas that need more attention.

-   Analyzing product
    risks early contributes to the success of a project.
    
#### What is the difference between Static and Dynamic Testing?
**Static**:
-   Under Static Testing, code is not executed. Rather it manually checks the code, requirement documents, and design documents to find errors. Hence, the name "static".

**Dynamic**:
-   Under Dynamic Testing, a code is executed. It checks for functional behavior of software system, memory/cpu usage and overall performance of the system. Hence the name "Dynamic".
#### Compare V-modell, Waterfall, Agile from testing perspective!
-   Agile testing is adopted while working with agile development approach whereas waterfall testing is used in the waterfall development model

-   V-model integrates the test process throughout the development process,
    implementing the principle of early testing. Further, the V-model includes test levels associated with each
    corresponding development phase, which further supports early testing.   

#### What would you test in case of a simple webShop purchasing function (put items to cart, buy them)? Plan and reason your tests.
-   proceed to buyout without item/s in cart.(we dont want to store orders without items)
-   to check if the user can buy two same item with one line(dont duplicate the same item in different line in the cart) 
-   to check the quantity cant goes into negative number(we dont want to buy "minus" items)
-   to raise/decrease the quantity in the cart , if we want modify it(user experience)
-   if quantity equal to zero , remove the item from the cart (to able to remove the item from the cart)  

### Reporting, Bugs

#### What steps would you follow when you find a defect?
Once a bug is found this should be communicated to the developer.
Before reporting the bug make sure that the bug is well documented with steps to repro,
conditions under which this bug is occurring,
how many time it occurs &  the excepted result of the bug.
The bug report should accurate & complete, so that developer can get the exact failure reason
#### Talk about common test reports, and about their details.
    During test monitoring and control, the test manager regularly issues test progress reports for
    stakeholders. In addition to content common to test progress reports and test summary reports, typical
    test progress reports may also include:
-    The status of the test activities and progress against the test plan
-    Factors impeding progress
-    Testing planned for the next reporting period
-    The quality of the test object

    When exit criteria are reached, the test manager issues the test summary report. This report provides a
    
    summary of the test.

#### What does a bug report contains?
-   **Bug Title**: This is the title of bug help to identify the bug in one-liner description.
-   **Bug identifier**: It is auto-generated unique ID helps to identify the bug.
-   **In the Bug** Tracking Tool, this field is auto-populated.
-   **Description**: This should cover bug description along with the exact Steps To Reproduce, Expected Result, Actual Result and example.
-   **Status**: This field indicates the actual status of the bug in the Bug life cycle.
    -   Here is the list of Bug Statuses in **standard Bug life cycle**:
        -   New 
        -   Assigned
        -   Resolved
        -   Reopened
        -  Verified (Vary based on Bug Tracking Tool)
-   **Bug Assignee**: This is the name of the developer who is responsible to resolve the bug.
-   **Bug Cc**: Add the manager and lead email address in CC list.
    In the Bug Tracking Tool, this field is auto-populated based on configuration.

-   **Reported On**: The date on which the bug is occurred & reported the bug.
-   **Browser**: This field indicates on which browser & version this issue occurs.
-   **Bug Type**: The bug is categories into a different category like Functional, Navigational, GUI etc.
-  **Environment**: On which OS, platform this bug occurs.
-   **Component**: This field indicates the sub-modules of the product.
-   **Priority**: Urgency to fix the bug?
    Priority can be set as P1 to P5.
    -   The P1 means “first fix this bug i.e. priority is highest” and P5 means “No urgent, when get time then fix it”.

-   **Severity**: This tells you about the impact of the bug.
-   **Types of Severity**:
    -   Blocker: Unless and until this fix no further testing can be done
    -   Critical: Application is crashing or Losing the data.
    -   Major: Major function under test is not working.
    -   Minor: Minor function under test is not working.
    -   Trivial: UI issues
    -   Enhancement: Asking for new changes as an enhancement.

#### How would you prioritize a bug?
Depend on the severity , what kind of bug is this?(Compared to a product)

### Test Automation, Selenium

#### Which test cases should be be automated and which shouldn't?
+   Do's:
    +   DO automate tasks as close to the code as possible
    +   DO automate repetitive tasks
    +   DO automate things users will do every day
    +   DO automate basic smoke-level tests
    +   DO automate things that will save you time
    +   DO automate things that will allow you to exercise lots of different options
    +   DO automate things that will alert you when something is wrong
-   Don't:
    -   DON’T automate tests that you know will be flaky
    -   DON’T automate tests for features that are in the early stages and are expected to go through many changes
    -   DON’T automate tests for features that no one cares about
    -   DON’T automate weird edge cases
    -   DON’T automate bugs you are sure will never be seen again
#### Describe a good automated test!
-   **Simple**
-   **Modular**
-   **Reliable**
-  **Reusable**
-  **Maintainable**
-  **Documented**
-  **Independent & Self-sufficient**
#### What is Selenium, Selenium IDE, Selenium WebDriver?
-   Selenium is an open source tool which is used for automating the tests carried out on web browsers.
    **Only testing of web applications is possible with Selenium**. 
    
-   We **can neither** test **any desktop (software) application** **nor** test **any mobile application** using Selenium.

-   Selenium IDE:
    -   By using selenium IDE user can record and playback test cases in a browser.
    
-   Selenium WebDriver:
    -   Selenium WebDriver tool is used to automate web application testing to verify that it works as expected. It supports many browsers such as Firefox, Chrome, IE, and Safari.
    -   also supports different programming languages such as C#, Java, Perl, PHP and Ruby for writing test scripts.
    -   is platform-independent since the same code can be used on different Operating Systems
    -    By using different jar files, we can also test API, Database Test etc. using Selenium WebDriver.    
#### How can be web elements identified?
-   selector
-   Xpath
-   jsPath
-   outerHTML 
#### How can you wait for elements, what can go wrong? Collect possible errors and root causes.
-   Implicit Wait:
    -   ``` driver.manage().timeouts().implicitlyWait(TimeOut, TimeUnit.SECONDS);```
-   Explicit Wait:
    -   ``` WebDriverWait wait = new WebDriverWait(WebDriverRefrence,TimeOut);```
-   Fluent Wait:
    -   ```
        Wait wait = new FluentWait(WebDriver reference)
        .withTimeout(Duration.ofSeconds(SECONDS))
        .pollingEvery(Duration.ofSeconds(SECONDS))
        .ignoring(Exception.class);
        ```
        
 -  Most of the web applications are developed using Ajax and Javascript. When a page is loaded by the browser the elements which we want to interact with may load at different time intervals.
 
-   Some errors:
    -   "ElementNotVisibleException"
    -   "NoSuchElementException"
#### Compare POM and Keyword Driven Testing!
-   Keyword Driven Testing(**KDT**):
    -   In Keyword Driven Testing, you first identify a set of keywords and then associate an action (or function) related to these keywords. Here, every testing action like opening or closing of browser, mouse click, keystrokes, etc. is described by a keyword such as openbrowser, click, Typtext and so on.
    
    -   A keyword-driven testing is a scripting technique that uses data files to contain the keywords related to the application being tested
    
    -   A keyword-driven testing usually performed by automated testing.
    
    -   Tests can be developed without programming knowledge


-   POM:
    -   Page Object Model is a design pattern to create Object Repository for web UI elements. Under this model, for each web page in the application, there should be corresponding page class. This Page class will find the WebElements of that web page and also contains Page methods which perform operations on those WebElements.
        
    -   It helps make the code more readable, maintainable, and reusable.
    
    -   Page Object Pattern says operations and flows in the UI should be separated from verification.
    
    -   Page Object Model is an Object Repository design pattern in Selenium WebDriver.
   
    -   POM creates our testing code maintainable, reusable.
   
    -   Page Factory is an optimized way to create object repository in POM concept.
  
    -   AjaxElementLocatorFactory is a lazy load concept in Page Factory pattern to identify WebElements only when they are used in any operation.

    
#### Whats the difference between TDD and BDD?
#### What is API testing and why would you use that?
#### What is Data Driven Testing and why is it useful?
-   **Data Driven Testing** framework resolves this problem by keeping the data separate from Functional tests.**The same test script can execute for different combinations of input test** data and generate test results.

-   Data-driven is a test automation framework which stores test data in a table or spread spreadsheet format.
    
-   **Frequently we have multiple data sets which we need to run the same tests on. To create an individual test for each data set is a lengthy and time-consuming process.**

-   Data Driven Testing framework resolves this problem by keeping the data separate from Functional tests. The same test script can execute for different combinations of input test data and generate test results.
#### What are the challenges and best practices with dynamically loading web elements?
#### What are the challenges of Mobile Test Automation?

### Advanced Topics

#### What is the difference between CI and CD?
#### Describe a Continuous Delivery!
#### Compare 2 popular CI systems, one of them should be Jenkins!
#### What is Docker, why is it useful?
#### Compare 2 popular Test Automation IDE, one of them should be Katalon Studio!