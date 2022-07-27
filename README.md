# The International Testing Standard (TITS) for DeFi

I believe that protocols need to be held to a higher standard of testing. Web3 protocols are decentralised, therefore there are no central authorities, and subsequently no regulatory pressure present to do quality checks on web3 software.

Is this such a big issue?
**YES**

These softwares (DeFi protocols) handle the hard earned money of everyday Joes like you and me (and also money of stupid funds like 3AC, but yeah, you get the point) so, we cannot let the protocols continue with lax testing.

It does not matter (much) how many auditors have had a stab at your protocol, you, as a developer, do not really understand if you protocol really works and is robust enough to take on the uncertainities of the real world if you have not tested your protocol thoroughly. 

Therefore, with this repository, I aim to create a certain set of testing standards that all DeFi protocols should strive to meet.

I plan to create this set of standards via iteration.
Iteration of publicaly critiquing leading DeFi protocols that are in use today, so that the up and coming protocols in the same space can get an idea and inspiration for the level of testing that the entire community expects out of a protocol that claims to handle money.

## List of protocols being evaluated

1. [Maple Finance](https://github.com/saxenism/defi-tits/tree/master/Maple%20Finance)

## Random tid bits about traditional testing that I have picked up...

This is definitely not molded for web3 yet, but consider this a good starting point if you haven't formally studied [Software Engineering](https://www.youtube.com/playlist?list=PLbRMhDVUMngf8oZR3DpKMvYhZKga90JVt).

Testing of software is an extremely imaginative and cognitively demanding task, more so in DeFi. So let your imagination go wild and gather ideas regarding testing from any walk of life, science, religion, parenting, social sciences, etc. Just about everything is fair game in testing.

## 1. Old wisdom related to testing

### 1.1 Presence of bugs
Testing can esure that defects are present but it cannot prove that a particular software is bug-free. Which isn't something super nice, but I'm coping too.

### 1.2 None can do exhaustive testing
Your software can never be tested for every imaginable and possible test cases. Trust me fellow crypto bro, you cannot.

### 1.3 Test Early
Earlier you test, lesser you'll cry.

### 1.4 Defect Clustering
Pareto principle but for origin of software bugs.

### 1.5 Pesticide Paradox
Don't be an idiot and test the same thing over and over with different methods. Find novel ways to screw with your protocol.

### 1.6 Testing is context-dependent
Every protocol does something special. Test the shit out of that.

### 1.7 Absence of errors fallacy
Just like your hot and caring girlfriend, a 100% bug-free software exists only in your imagination.


## 1. Why testing is important

+ Saves you and your users from getting rekt.
+ Hoping for your protocol's success without adequate testing is like going into a gunfight without a bulletproof vest and hoping you don't get shot.
+ Time and effort spent on testing can be leveraged to get better terms when you get your protocol insured.
+ In short, you'll get your lambo only wen you test.

Thank you for coming to my TED talk. Bye.

## Types of testing

Functional and Non Functional

Non Function includes 
- Testing the Documentation (which includes)
    - Instructions
    - Examples
    - Messages
    - Samples
- Installation Testing
- Performance Testing
    - Load Testing
    - Spike Testing
    - Stress Testing
    - Endurance Testing
- Reliability Testing
    - Feature Testing
    - Regression testing
    - Load Test
    - Objectives Testing
- Security Testing (web2 stuff)
    - Access to application
    - Data Protection
    - Brute FOrce
    - SQL Injection
    - Service Point
    - Session Management
    - Error Handling
    - Specific Risky Functionalities

## 2. SDLC

+ Requirement
+ Analysis (outcome from this phase is SRS)
+ Design (HLD and LLD)
+ Coding
+ Testing
+ Deployment and all

### 2.1 Waterfall Model

Sequential design process. One way street, so back tracking is not possible.

![Waterfall Model Image](https://www.tutorialscampus.com/sdlc/img/waterfall-model.png)

### 2.2 Spiral Model

Combination of iterative development process model and sequential linear development model.

![Spiral Model Image](https://pbs.twimg.com/media/DJxUCFeVoAA5bt1?format=jpg&name=small)

## 3. Validation vs Verification

| Verification                           | Validation                       |
| -----------                            | -----------                      |
| Methods involve: review, inspection, unit testing & integration testing| Involves testing the entire system (system testing)                            |
| Usually done by developers while developing                              | Usually done by tester and after developing of the product by developers                             |
|Concerned with the phase containment of errors | Concerned with making the final product error free |
| Involves static and dynamic analysis of code | Involves only dynamic analysis of code |

## 4. Types of software testing

### 4.1 Unit Testing

Can be done in the development phase itself. Unit means a particularly small piece of (preferrably independent) code such as a function, small module etc.

Smallest element of the software is a unit and testing each of those units is **unit testing**.

### 4.2 Integration Testing

Combine different units of code and test whether they work together as expected to produce the desired output or not.

4 common integration testing startegies are as follows:

#### 4.2.1 Big Bang Testing

All units are linked at once, resulting in a complete system. Here, it is difficult to isolate any errors found.

#### 4.2.2 Top Down 

Higher level modules are tested first after which the lower level modules are tested. Higher level modules refer to the main modules and lower level refers to the sub modules.

**Stubs** (temporary modules) are used to simulate the behaviour of the lower-level modules that are not yet integrated. 

Used when software needs to interact with an external system.

#### 4.2.3 Bottom Up

Lower level modules are tested first and then the higher level modules. 

This approach uses **test drivers** which are mainly used to initiate and pass the required data to the sub modules, implying we pass mock data that should ideally have come from (the not yet implemented) higher modules.

#### 4.2.4 Mixed (Sandwiched integration testing)

A mixed integration testing follows a combination of top down and bottom-up testing approaches.

### 4.3 System Testing or End-to-End Testing

Testing the entire system. Here, we navigate all the necessary modules of an application and check if the end features or the end business works fine, and test the product as a whole system.

#### 4.3.1.1 Alpha Testing

+ The testers are people who have built the product.
+ Done before releasing the product.
+ Involves both white box and black box testing

#### 4.3.1.2 Beta Testing

+ Beta testing is performed by a select set of clients who are not part of the organization. 
+ User input on the product is collected to ensure the product is ready for real time users
+ Commonly involves only black box testing

#### 4.3.2 Acceptance Testing

It is a formal testing according to user needs, requirements and business processes conducted to determine whether a system satisfies the acceptance criteria or not and to enable the users, customers or other authorized entities to determine whether to accept the system or not.

##### Smoke Testing or Build Verification Testing

+ Subset of acceptance testing

| Smoke Testing | Sanity Testing |
|----------------|----------------|
| Smoke testing is done to assure that the acute functionalities of program is working fine. | Sanity testing is done to check the bugs have been fixed after the build. |
| Smoke testing is documented. | Sanity testing isn’t documented. |
| Smoke testing is done to measures the stability of the system/product by performing testing. | Sanity testing is done to measures the rationality of the system/product by performing testing. |
| Smoke testing can be performed either manually or by using automation tools. | Sanity testing is commonly executed manually, not by using any automation approach. |
| Smoke testing is used to test all over function of the system/product. | Sanity testing is used in the case of only modified or defect functions of system/products. |
|Smoke testing is performed when new product is built. |Sanity testing is conducted after the completion of regression testing.|


#### 4.3.3 Mutation Testing

+ Type of white box testing
+ Extremely costly and time consuming but also extremely efficient in finding errors and ambiguities
+ In this type of testing, you slightly change the value/logic/statements in your code and see if you get the expected output in your tests

#### 4.3.4 Performance / Non functional Testing

Non-functional testing is defined as a type of software testing to check non-functional aspects of a software application. It is designed to test the readiness of a system as per nonfunctional parameters which are never addressed by functional testing.

This testing tests the following things (among others):
+ Volume
+ Load
+ Stress
+ Security
+ Configuration 
+ Compatibility (BrowserStack :P)
+ Recovery
+ Installation etc

#### 4.3.5 Recovery Testing in Software Testing

+ Recovery testing is a type of system testing which aims at testing whether a system can recover from failures or not.
+ To ensure that a system is fault-tolerant and can recover well from failures, recovery testing is important to perform.

### 4.4 Regression Testing

Regression testing is the process of testing the modified parts of the code and the parts that might get affected due to the modification to ensure that no new errors have been introduced in the software after the modifications have been made.

#### 4.4.1 Techniques for the selection of test cases for regression testing

+ Select all test cases (Most thorough but inefficient approach)
+ Select test cases randomly (Dangerous approach)
+ Select modification traversing test cases (Huge upfront work required to identify these test cases)
+ Select higher priority test cases (Assign priority values to all your tests, then re-test all your highest priority tests)

#### 4.4.2 Sanity Testing

+ Subset if regression testing
+ Done to ensure that the code changes that have been made are working properly or not
+ Focus of the team during sanity testing is to validate the functionality of the application and not detailed testing
+ Usually performed on builds where the production deployment is required immediately like a critical bug fix.
+ Performed only after the software product has passed the smoke test and the QA team has accepted for further testing

## 5. STLC (Software Testing Life Cycle)

+ Requirement Analysis (Truly truly understand what your protocol is supposed to do)
+ Test Planning / Strategy Phase (Based on the context of the protocol in question, zero in on a testing strategy)
+ Test Case Development (This should take the maximum amout of time. List down all test cases that you think are appropriate.)
+ Environment Setup (Independent of other stages) (Don't tell me you don't already have Forge installed)
+ Test Execution (Code up all the test cases you came up with earlier. You can do back and forth between Test Execution and Case Development phase, but try to keep it minimal)
+ Test Cycle Closure (Create a good report. Remember, chads keep their work presentable)

## 6. Non Functional Testing

+ This is based on customer expectations as opposed to functional testing which is based on customer requirements.
+ Non functional testing describes how the product works rather that what the product does
+ Includes things like performance testing, scalability, volume testing, load testing, stress testing etc.

### 6.1 Performace Testing

+ Ensures software application will perform well under their expected workload
+ Goal is not to find bugs but to elimiate performance bottle-necks
+ Provides accurate information about the speed, scalability and stability of the software
+ Types of performance testing types
    + Load Testing (Multiple users access application simultaneously)
    + Stress Testing
    + Endurance Testing
    + Spiking Testing
    + Volume & Scalability Testing 
+ Pay attention to:
    + Long load time
    + Poor response time
    + Poor scalability
    + Bottlenecking
+ Examples of performance Test cases:
    + Verify response time is not more than 4 seconds when 1000 users access the website simultaneously 
    + Check the maximum number of users that the application can handle before it crashes
    + Verify response time of the application under low, normal, moderate and heavy load conditions

### 6.2 Cross browser Tests and Mobile Testing and API Testing

See if this is applicable and test if you have the resources to do so.

Types of API Testing

+ Functionality Testing
+ Reliability Testing
+ Load Testing
+ UI/UX Testing
+ Interoperability Testing
+ Security Testing
+ Penetration Testing
+ Negative Testing

## 7. Agile Testing (Test Driven Development (TDD))

+ Testing is continuous
+ Continuous Feedback
+ Decreased time of feedback response
+ Less documentation
+ Test Drive
+ Simplified Code

![](https://i.imgur.com/8oKMUr3.png)


## 7. Software Testing Documentation

### 7.1 Test Plan

Provides the outline strategy which will be implemented for testing the application and also the resources that will be required. Test environement will also be described.

Make sure that you also set up a *defect/bug life cycle*

### 7.2 Test Scenario

Notifies the area in which your application will experiment

### 7.3 Test Case

Collected steps and conditions with inputs that can be implemented at the time of testing. 

### 7.4 Traceability Matrix

A table where you can relate test case IDs with protocol requirement IDs. 

## 8. Defect Management Process (What to do when you find bugs)

+ Detect the defect
+ Formulate the bug report
+ Fix bug
+ Bug list creation (so that, yk, history doesn't repeat itself and everyone sees that you have 3 brain cells)

It is important to note in the first two points, whenever you encounter a bug, you have to reach to the root cause of the bug and report that. Because, it is very much possible that the actual coding error that caused the bug might create many more bugs in the future.

In short, treat the root cause and not just the symptoms.

## 9. When to choose manual testing

### 9.1 Exploratory Testing

Carried out by domain experts.
Minimal planning

### 9.2 Usability Testing

User friendliness of an app

### 9.3 Ad Hoc Testing

Informal testing.
No documents are followed.

### 9.4 How to do manual testing
1. Understand the requirements
2. Write the test cases
3. Conducting the tests
4. Log Good Bug Reports
5. Report the results (Detailed test report)

## What to automate?

+ Repetitive Task
+ Capturing Results
+ Data Entry Tasks
+ Timing or Screening Responsiveness
+ Non functional Testing
+ Environment Setup/Tear down

## Approaches to Test Automation (Look them up)

+ Code driven Testing
+ Graphical User Interface
+ Framework Approach
    + Linear Scripting framework
    + Data driven framework
    + Keyword driven framework
    + Modular testing framework
    + Hybrid Testing Framework


