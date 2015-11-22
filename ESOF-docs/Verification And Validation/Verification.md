4. Verification and Validation 
===================

1) Degree of Testability of the software program
Topics: Discuss how 'testable' is the program. Discuss how to improve the testability of software components.

The testability of software components (modules, classes) is determined by factors such as:
- Controllability: The degree to which it is possible to control the state of the component under test (CUT) as required for testing.
 
- Controllability ??
- Observability: The degree to which it is possible to observe (intermediate and final) test results.

- Observability - Well explicit. Information about what module is being tested and even a traceback will be displayed in the console with appropriate and noticeable separation. In the end of the test run a compilation of final results (mostly statistical) will also be displayed.
 
- Isolateability: The degree to which the component under test (CUT) can be tested in isolation.

- Isolateability: It is possible to run tests on a specific module by adding module name as the last argument when running the test suite. One can also state the directory where the specific tests one wants to run are stored.
 
- Separation of concerns: The degree to which the component under test has a single, well defined responsibility.
 
- Separation of concerns: Altough the current test name is displayed it may sometimes not suffice to properly identify what is being tested but mostly the tests have a good separation of concerns given that they are as unitary as possible. As a matter of fact, Django's creators themselves clearly specify in the documentation that:
> Generally tests should be:

>    Unitary (as much as possible). i.e. should test as much as possible only one function/method/class. That’s the very >definition of unit tests. Integration tests are interesting too obviously, but require more time to maintain since they have a >higher probability of breaking.
    
And they seem to follow their own advices.

- Understandability: The degree to which the component under test is documented or self-explaining.

- Understandability: As stated, altough sometimes test names alone are not enough to accurately identify what component exactly is being tested, it is also displayed which test exactly is being ran so a quick peek on the test code - only in the few cases of need for clarification - should be enough to fully understand the running test.
 

- Heterogeneity: The degree to which the use of diverse technologies requires to use diverse test methods and tools in parallel.
- Heterogeneity: The most recent test suite for Django-cms includes diverse tools such selenium (http://www.seleniumhq.org/), sphinx (http://sphinx-doc.org/), pyenchant(http://pythonhosted.org/pyenchant/) and others as specified in https://github.com/SofiaReis/django-cms/blob/develop/test_requirements/requirements_base.txt but as some tools are purely aesthetic the main testing tool would be Selenium.

##4.1. How is Django-CMS tested?

##4.2. How to improve software test?


##4.3. Coverage Statistics
     Number of tests (# tests unitários; # tests de sistema, # tests de desempenho, ...)
     % coverage (given by tools like EclEmma)
     Code coverage: is it any good? (see http://avandeursen.com/2013/11/19/test-coverage-not-for-managers/)


##4.4. Bug Report
3) [Opcional] Take a bug report, create test cases to reproduce it, and fix it, eventually using automated software fault diagnosis techniques. (grade >18)