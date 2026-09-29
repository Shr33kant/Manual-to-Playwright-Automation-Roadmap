###### **PHASE 1 — SOFTWARE TESTING FUNDAMENTALS**



**MODULES 1 — Introduction to Software Testing**



**Learning Objective:**

What is Software?

What is Software Testing?

Why Do We Need Testing?

Objectives of Software Testing

Role of a Software Tester

Software Testing in the SDLC

\------------------------------------------------------------



1. **What is Software?**
* Software is a set of programs, instructions and related data that tells computer or device what to do.

&#x20;A software application normally has: **User → Application → Backend → Database**

**Examples:** Amazon, WhatsApp, Netflix, Banking Apps, Food delivery apps



**2. What is Software Testing?**

* Software testing is the process of evaluating the software to validate whether the software fulfills the requirements and specifications and whether it behaves as expected it is not only limited to finding the bugs.
* In simple words, we test software to find problems and verify that it works according to requirements.
* **Development creates the software; testing provides evidence about whether the software behaves as expected.**



**Example:** Suppose a developer creates a login page.

&#x09;	**Requirement:** User should be able to log in using valid username and valid password.

&#x09;As a tester, we don't simple login once and say it's working.

&#x09;QA asks questions like:

What happens with valid username and Password?

What happens with Invalid username and password?

What happens with blank username?

What happens with blank password?

What happens with both fields blank?

What happens after multiple failed attempts?

**Verifying all these possibilities (Scenarios) is called Testing!**

Testing is not just *"checking whether it works."*

Testing means: *Checking different conditions and comparing actual behavior with expected behavior.*



**A. Manual testing:** Manual testing involves a human tester evaluating an application's design, functionality, and performance by following test cases without relying on automation tools.

&#x09;**\* Advantages of Manual Testing**

* **Live Testing Conditions:** Evaluates the application under real-world conditions that closely mirror live usage, making it easier to track bugs or glitches that appear post-launch.
* **Visual \& Usability Testing:** Ideal for catching look-and-feel issues, design flaws, and user-friendliness problems that automated scripts might miss.
* **Low Initial Investment:** Does not require costly tools or high-level technical setup initially, making it cost-effective for short-term scenarios.
* **Flexibility for Changes:** Allows for swift testing and immediate outcomes when an application undergoes unplanned, rapid changes.



**B. Automation testing:**  Automation testing uses scripts and tools to execute tests automatically. Automation is particularly useful for repetitive and regression testing.

&#x09;**\* When is Automation useful?**

Especially for:

*Repetitive testing*

*Regression testing*

*Large numbers of test cases*

*Frequently executed tests*

*Faster execution*



**3. Why Do We Need Software Testing?**

Imagine a banking application without proper testing.

A user has a account balance of ₹10,000. But because of a software defect customer can transfer any amount suppose instead ₹10,000 he is able to transfer ₹100,000.

That's a serious problem, and will turn into financial loss to bank. And this is just an example, delivering software without Testing can Impact business, user experience, and waste time and cost.



**4. Common reasons for testing/ Objectives of testing**

**A. Review requirements:** Review the requirements before starting the testing.

**B. Verify requirements:** Check whether implemented feature/software fulfills the requirements and specifications

**C. Find defects** before it reaches the final users.

**D. Validate functionality:** Check whether the application behaves correctly for the intended use.

**E. Reduce business risk:** Find problems before they cause business/customer impact.

**F. Improve software quality:** Testing helps identify areas where the software doesn't behave correctly.

**G. Improve user experience by identifying problems such as:**

&#x09;Broken buttons

&#x09;Incorrect messages

&#x09;Crashes

&#x09;Incorrect calculations

&#x09;Navigation problems

&#x09;Slow responses

&#x09;Security-related issues

**H. Provide information:** Testing provides information about the quality and behavior of the software.



**5. What Does a Software Tester Actually Do?**

A tester's job isn't simply: Click buttons and check just the functionality.

A typical tester may:

**Understand req. > Identify what needs testing > Create test scenarios > Create test cases > Prepare test data > Execute tests > Compare expected vs actual result > Report defects > Retest fixes > Perform regression testing > Report testing status**

Later in Automation:

**Manual Test Case > Identify repetitive tests > Automate using Playwright  > Write automation script > Execute > Assertion > Pass / Fail > Report testing status**



So automation testing doesn't replace manual testing knowledge. It automates the execution of selected tests.

\------------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Practical Example — E-commerce Application**

Imagine you're testing an Amazon-like shopping application.

**Requirement:** User should be able to add a product to the cart.

A beginner tester might do: *Open website > Select product > Product appears in cart > Done.*

But a Professional tester should think:

**Positive Test cases:** Product available → Add to Cart → Product added

**Negative Test cases:** 

1. Product out of stock → Add to Cart → What should happen?
2. User not logged in → Add to Cart → What should happen?
3. Network interruption → Add to Cart → What should happen?
4. Click Add to Cart multiple times → What happens?



**This is where testing mindset begins.**

\------------------------------------------------------------------------------------------------------------------------------------------



**ASSIGNMENT 1**

Let's assume you are testing a simple Login Application. The login screen contains:

\---------------------------------------------------

**Email:    		\[\_\_\_\_\_\_\_\_\_\_\_\_]**

**Password: 	\[\_\_\_\_\_\_\_\_\_\_\_\_]**

&#x20;           **\[ LOGIN ]**

\--------------------------------------------------

**Requirement**: A registered user should be able to log in using a valid email and password.

Think like a tester and identify at least 8 different things you would test.

**Ans:**

1. Login with Valid Email and Password
2. Login with Invalid Email
3. Login with Invalid Password
4. Login with Blank Field in Email
5. Login with Blank Field in password
6. Login with both Invalid Email and Password
7. Login With both Email and Password fields empty
8. Login without registering a user/ unregistered user
9. Login using only special characters in Password
10. Login with SQL Injection query
11. Login with Java Program

\--------------------------------------------------------------------------------------------



**ASSIGNMENT 1**

**Requirement:** "An ATM allows a customer to withdraw cash from their bank account."

