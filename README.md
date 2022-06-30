# DeFi TITS

Testing of software is an extremely imaginative and cognitively demanding task, more so in DeFi.

Testing is an art form.

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

### 4.4 Regression Testing

Regression testing is the process of testing the modified parts of the code and the parts that might get affected due to the modification to ensure that no new errors have been introduced in the software after the modifications have been made.

#### 4.4.1 Techniques for the selection of test cases for regression testing

+ Select all test cases (Most thorough but inefficient approach)
+ Select test cases randomly (Dangerous approach)
+ Select modification traversing test cases (Huge upfront work required to identify these test cases)
+ Select higher priority test cases (Assign priority values to all your tests, then re-test all your highest priority tests)

