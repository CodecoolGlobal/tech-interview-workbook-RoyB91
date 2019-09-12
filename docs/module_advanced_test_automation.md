# Test automation questions

### Testing Basics (ISTQB related)

#### What is the purpose of testing? What is not?
    Testing verifies that the system meets the different requirements including,
    functional, performance, reliability, security, usability and so on.
    This verification is done to ensure that we are building the system right.
    
        What is not:
            -   to ensure the software is not good product
            -   to blame the developers who wrote the code
             
#### What is the difference between Defect, Error, Failure?
-   Defect:
     It can be simply defined as a variance between expected and actual. Defect is an error found AFTER the application goes into production.
     It commonly refers to several troubles with the software products,
     with its external behavior or with its internal features.

-   Error:
    An error is a mistake, misconception, or misunderstanding on the part of a software developer.
    In the category of developer we include software engineers, programmers, analysts, and testers. 
    
-   Failure:
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
        defect clusters in test or operation, are an important input into a risk analysis used to focus the test effort.
  
  - **Beware of the pesticide paradox**:
    -   To detect new defects, existing tests and test data may need changing, and new tests may need to be
        written.
    -   In some cases, such as automated regression testing, the pesticide paradox has a
        beneficial outcome.
  
  - **Testing is context dependent**:
    -   Testing is done differently in different contexts.
    
  - **Absence-of-errors is a fallacy**:
    -   Overall important to give a customer what he/she want , a working products.(not mayor bugs,etc.)

#### What is unit testing? Who is responibile to write unit tests?
#### What are Test Levels, what is the difference between them?
#### What is the difference between verification and validation?
#### What are Testing Types, what is the difference between them?
#### What is the difference between white box, grey boy and black box testing?
#### What is the difference between UAT (User Acceptance Testing) and System testing?
#### Mention the differences between Regression Testing, Smoke Testing and Retesting?
#### What is risk-based testing, whats the point of it?
#### What is the difference between Static and Dynamic Testing?
#### Compare V-modell, Waterfall, Agile from testing perspective!
#### What would you test in case of a simple webshop purchasing function (put items to cart, buy them)? Plan and reason your tests.

### Reporting, Bugs

#### What steps would you follow when you find a defect?
#### Talk about common test reports, and about their details.
#### What does a bug report contains?
#### How would you prioritize a bug?

### Test Automation, Selenium

#### Which testcases should be be automated and which shouldn't?
#### Describe a good automated test!
#### What is Selenium, Selenium IDE, Selenium WebDriver?
#### How can be web elements indentified?
#### How can you wait for elements, what can go wrong? Collect possible errors and root causes.
#### Compare POM and Keyword Driven Testing!
#### Whats the difference between TDD and BDD?
#### What is API testing and why would you use that?
#### What is Data Driven Testing and why is it useful?
#### What are the challenges and best practices with dynamically loading web elements?
#### What are the challenges of Mobile Test Automation?

### Advanced Topics

#### What is the difference between CI and CD?
#### Describe a Continuous Delivery!
#### Compare 2 popular CI systems, one of them should be Jenkins!
#### What is Docker, why is it useful?
#### Compare 2 popular Test Automation IDE, one of them should be Katalon Studio!