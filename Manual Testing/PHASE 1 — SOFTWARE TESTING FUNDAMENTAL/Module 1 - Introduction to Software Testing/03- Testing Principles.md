###### **03- Testing Principles**



* **FUNDAMENTAL TESTING PRINCIPLES**

There are several fundamental principles that explain how the Software Testing actually works.



1. **Testing shows the Presence of Defects, not their absence**
Testing can demonstrate that defects exists in software, but testing cannot prove that the software is 100% bug-free.
EXAMPLE: We test a login application with:
*Valid Email + Vaild Password
Invalid Email
Invalid Password
Black Fields*
Everything passes. But still we cannot conclude that there are absolutely no defects in the login application.
We just have demonstrated that the tested conditions have passed i.e. behaved correctly.
But it does not mean that the Login Functionality is completely bug free. There could still be an undiscovered defect under another conditions.
2. **Exhaustive Testing is Impossible.**
We cannot test **every possible combination** of inputs, environments, devices, users, data, etc. for most real-word applications.
EXAMPLE: Imagine a simple login form,
*Email
Password*
Now Consider:
*Different Email formats, different Password lengths, Different Characters
Invalid values, Empty Values
Different Browsers, Different OS, Different user states*
**The combination becomes enormous.**
Therefore, testers select **representative and important conditions** rather than testing every possible combination.
3. **Early Testing**
Testing activities should begin **as early as possible** in the SDLC. Testing is not something that should start only after development is finished.
EXAMPLE: During requirements,
**Requirement:** *Application should respond quickly.*
Testers/QA asks: What does **quickly** mean? Do we have a response-time requirement?
If this ambiguity is discovered before development, it can be clarified early which will save time, efforts and cost comparative to Starting and finding defects in later stages. This connects directly to the **Defect Economics.
Hence, the earlier the problem is identified, the easier it is generally to address.**
4. **Defect Clustering**
Defects are often **not evenly distributed** throughout an application. A relatively **small number of components** may contain **a large proportion of the defects**.
EXAMPLE: An E-commerce application has,
*Login, Product Search, Product details, cart, payment, Order History, Profile.*
Testing reveals:
*Login           	→ 2 defects
Search          	→ 1 defect
Product Details → 1 defect
Cart            	→ 3 defects
Payment         	→ 15 defects
Profile         	→ 1 defect*
**Payment appears to be the module that contains significantly more defects.**
Hence that area may require additional attention.
**IMPORTANT:**
In this example, payment module has the most number of defects, but it doesn't mean that Payment always have the most defects.
**It simple means, defects often tend to cluster in certain components or areas.**
5. **Pesticide Paradox**
If we repeatedly execute exactly the same tests over and over, eventually those tests may stop finding new defects, just like the, just like using the same chemical pesticide repeatedly makes pests immune to it.
Imagine you have these five tests:
*Login with valid credentials
Login with invalid password
Blank username
Blank password
Logout*
If we execute the same tests everyday, they continue passing.
Does that mean there cannot be other defects?
No. In this scenario, we may need to introduce new test conditions.
EXAMPLE:
*Password boundary values
Special Characters
Session Timeout
Multiple failed login attempts
Different browsers*
**Hence, Repeatedly running the same tests may become less effective at finding new defects, so tests should be reviewed and enhanced over the time.** That's called **Pesticide Paradox.**
6. **Testing is Context dependant**
There is no single testing approach that works identically for every application.
Testing depends on:
*Type of application
Business domain
Risk
Users
Requirements
Technology
Regulatory requirements
Environment*
EXAMPLE:

   1. In a **Banking Application** we may emphasize on-
*Security
Transaction accuracy
Data integrity
Reliability
Auditability*
   2. In **Gaming Application**, we may emphasize on:

&#x09;	*User experience*

&#x20; 		*Performance*

&#x09;	*Compatibility*

&#x20;		*Graphics*

&#x20;		*Responsiveness*

&#x09;*3.*	In **Medical Application**, we may have strong emphasize on:

&#x09;	*Safety*

&#x20;		*Accuracy*

&#x20; 		*Reliability*

&#x20; 		*Regulatory requirements*

&#x09;**So, Testing must be adapted to the context of the software being tested.**



**7.	Absence of error fallacy**

&#x09;Even if the software has no known defects, it can still fail if it doesn't meet user or business needs.

&#x09;**Example:**

&#x09;Imagine a shopping app, everything works perfectly. No defects. But, Customer can't search for products.

&#x09;Technically, the software may be "bug-free." Business-wise, it's a failure because it doesn't solve the user's 	problem.

\------------------------------------------------------------------------------------------------------------------------------------------------------------



* **HOW  MUCH TESTING IS ENOUGH?**



This is an important real-world question.

Suppose you have: **10,000 test** possibilities, But  have only **2 days** testing.

In this scenarios, we cannot execute 10,000 tests in just 2 days.

**So how do you decide what to test?**

We consider factors such as:

* *Business importance*
* *Risk*
* *Probability of failure*
* *Impact of failure*
* *Customer usage*
* *Regulatory requirements*
* *Available time/resources*



**Example:**

1. **Payment functionality**

*Failure impact: Very high*

*Therefore: Give it significant testing attention.*



2\.    **Change profile-picture functionality**

*Failure impact: Potentially much lower.*

*Therefore: It may receive less testing priority than payment.*



These scenarios leads to **Risk-Based Testing**\*.\*



* **RISK-BASED THINKING**



A tester shouldn't simply ask: "What can I test?"

A better question is: "What could go wrong, and what would happen if it did?"

Think about:

&#x09;**Risk = Probability × Impact**

We don't need to treat this as a precise mathematical calculation in every project. But, it's a way to think about prioritization.



EXAMPLE:

\-------------------------------------------------------------------------------------------------

| 	Feature         	| Probability of problem 	| Impact    	|

| ---------------------------- | ------------------------------------ | -------------------- 	|

| Login           		| Medium                 	| High      		|

| Payment         	| Medium                 	| Very High 	|

| Profile picture 	| Medium                 	| Low       	|

| About Us page	| Low                    		| Very Low  	|

\--------------------------------------------------------------------------------------------------



**Higher Risk areas need greater testing attention.**

**=========================================================================**



* **TESTER ROLE**

Now let's understand what a tester actually does.



**1. Role of a Tester**

A testers role is broader than just **finding the bugs.**

A tester helps the team understand:

* *Whether requirements are testable*
* *Whether the product behaves as expected*
* *What risks exist*
* *What defects were discovered*
* *What areas have been tested*
* *What areas remain risky*



A tester provides **information about the quality and risk of the product.**



**2. Tester Responsibilities**



**A. Requirement Analysis**

Understand:

* *What is being built?*
* *What should it do?*
* *What are the acceptance criteria?*
* *Are there ambiguities or missing details in requirements?*



**B. Test Planning**

Determine:

* *What needs to be tested?*
* *What is the scope?*
* *What environments are needed?*
* *What resources are required?*



**C. Test Design**

Create appropriate testing conditions, formal test scenarios and test cases.



**D. Test Execution**

Execute tests and compare:

*Expected Behaviour* vs *Actual behaviour*



**E. Defect Reporting**

When a problem is found:

*Identify **→** Reproduce <b>→</b> Document <b>→</b> Report*



**F. Retesting**

After developer fix a defect, verify that the specific issue has been resolved.



**G. Regression Testing**

Check that changes haven't unintentionally broken existing functionality.



**3. Tester Mindset**

A tester shouldn't think: *"How do I prove that this works?"*

A tester should also think: *"How could this fail?"*



Suppose the requirement says: *User can withdraw money.*

A basic mindset: *Can I withdraw ₹1,000?*

Whereas a tester's mindset expands:

* *What if balance is insufficient?*
* *What if ATM has insufficient cash?*
* *What if PIN is wrong?*
* *What if card is expired?*
* *What if amount is zero?*
* *What if amount is negative?*
* *What if amount exceeds daily limit?*
* *What if network connection fails?*
* *What if the user cancels the transaction?*



Remember, at this point we're not formally learning test-design techniques yet.

We're developing the mindset that will later make those techniques easier.



**4. Tester Involvement Across SDLC**

A tester isn't necessarily involved only when coding is finished.

Let's take a simplified SDLC:

*Requirements*

&#x20;    *↓*

*Design*

&#x20;    *↓*

*Development*

&#x20;    *↓*

*Testing*

&#x20;    *↓*

*Release*

&#x20;    *↓*

*Maintenance*



A tester can contribute throughout these stages.



1. **Requirements**

Tester:

* *Reviews requirements*
* *Identifies ambiguity*
* *Identifies missing information*
* *Checks whether requirements are stable*
* *identifies potential risks*



**2. Design**

Tester can review:

* *Application Flow*
* *UI Design*
* *Architecture/design decisions*
* *Error handling*
* *Testability*



**3. Development**

Tester may:

* *Clarify requirements with developers*
* *Prepare test conditions/data*
* *Review builds*
* *identify areas requiring additional testing*
* *Collaborate with developers*



**4. Testing**

This is where testers typically perform activities such as:

* *Execute tests*

&#x09;     *↓*

* *Compare expected vs actual*

&#x09;     *↓*

* *Identify defects*

&#x09;     *↓*

* *Report defects*



**5. Release**

Testers contribute information such as:

* *What has been tested?*
* *What passed?*
* *What failed?*
* *What defects remain?*
* *What risks remain?*

This helps stakeholders make informed release decisions.



**6. Maintenance**

After release:

* *Test bug fixes*
* *Perform regression testing*
* *Test enhancements*
* *verify production related fixes*



**#Tester Across SDLC — Mental Model**



**REQUIREMENTS**

&#x20;    **↓**

*Review \& clarify requirements*

&#x20;    **↓**

**DESIGN**

&#x20;    **↓**

*Review \& identify risks*

&#x20;    **↓**

**DEVELOPMENT**

&#x20;    **↓**

*Collaborate \& prepare*

&#x20;    **↓**

**TESTING**

&#x20;    **↓**

*Execute tests \& report data*

&#x20;    **↓**

**RELEASE**

&#x20;    **↓**

*Provide quality/risk information*

&#x20;    **↓**

**MAINTENANCE**

&#x20;    **↓**

*Retest \& regression*



**This is why modern testers are not simply "people who test after developers finish."**

**============================================================================**



**Practical Exercise — Risk-Based Thinking**



Q1. Imagine you're testing an online banking application with:

1\. Login

2\. View Account Balance

3\. Transfer Money

4\. Change Profile Picture

5\. Download Statement

For each feature, think about: *Probability of defect + Impact if defective*



Feature				Probability of Defect		Impact

Login				Medium				High

View Account balance	Low					Low

Transfer Money			Very High				Very High

Change Profile Picture	Very Low				Very Low

Download Statement		Medium				High



Q.2 Identify Which two areas would you give the most testing attention? Why?

Higher testing Attention areas/Features:

1. Transfer money feature deserves the highest testing attention. Because- Its impact on business is relatively higher than all other features as it directly involves the financial transaction which makes it extremely critical.

Login: After Transfer Money Login is, I think 2nd area which deserves higher attention because all other features related to Banking Application are depended on it. And that's make it business critical. 



**PRACTICAL EXERCISE — Tester Mindset**

Consider this requirement: "A user should be able to reset their password using their registered email address."

Without writing formal test cases, tell me at least 8 questions a tester should think about.

Remember: We're testing your thinking, not test-case-writing skills.

For example:

*What happens if the email is not registered?*

*What happens if user forgets the registered email address?*

*What is the maximum number of attempts to reset the password?*

*How email is used for password reset? With an OTP or Direct link verification? What if OTP/link is not received?*

*What if an unauthorized person tries to change the password having the email access? Is there any Multi factor Verification needed?*

*Can user reset the password multiple times if he forgets again and again?*



101843615205





