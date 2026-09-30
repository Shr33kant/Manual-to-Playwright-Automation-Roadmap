###### **TOPIC 2 - SOFTWARE QUALITY \& DEFECTS**



**A. DEFECT TERMINOLOGY:**

**1. Error:** An error is a human mistake made while creating or working on a software.

It can happen during:

&#x09;Requirement analysis

&#x09;Design

&#x09;Coding

&#x09;Configuration

&#x09;Testing

**Example**

A developer is implementing a tax calculation requirement: **Tax should be calculated at 18%.**

Developer accidentally writes: **Tax = amount \* 0.08**

Here, The developer has made a mistake and this mistake is an called an **error**.

**So, Error = Human mistake**



**2. Defect:** A defect is the flaw in an application that causes the implemented behaviour differ from the expected requirement/behaviour.

**Continuing our example:**

Requirement: **Tax = 18%**

Implementation: **Tax = 8%**

This incorrect implementation is a **defect**.

**So, Defect = A flaw in the software caused by an error.**



**3. Bug:** In everyday software development, bug and defect often used interchangeably.

For example, a tester may say: "I found a bug in the login functionality."

Technically, some organizations distinguish their terminology, but for your interview preparation:

**Bug is commonly used as another term for a defect.**



**4. Failure:** A failure occurs when the software actually behaves incorrectly during execution.

In other words:

If the defect exists in the software, and when a particular condition causes it to execute, the user/system observes incorrect behavior which is called as failure.



***Error vs Defect vs Failure***

Think of the below chain:

**Human makes a mistake**

&#x20;       **↓**

&#x20;     **ERROR**

&#x20;       **↓**

**Mistake gets introduced into software**

&#x20;       **↓**

&#x20;    **DEFECT**

&#x20;       **↓**

**Software executes under affected condition**

&#x20;       **↓**

&#x20;    **FAILURE**

**-----------------------------------------------------------------------------------------------------------------------------------------**

**| Term        	| Meaning                                      				|         Where? 	|**				

**| -------------------- | ---------------------------------------------------------------------------- | ---------------------------- |**

**| \*\*Error\*\*   	| Human mistake                                			| Person         		|**

**| \*\*Defect\*\*	| Flaw introduced into software                		| Software       	|**

**| \*\*Bug\*\*     	| Common term for defect                       		| Software       	|**

**| \*\*Failure\*\*	| Incorrect behavior observed during execution 	| Running system 	|**

&#x20;**----------------------------------------------------------------------------------------------------------------------------------------**



**Remember: Error → Defect → Failure**

But Not every defect necessarily produces a failure.

A defect might remain hidden until the software executes a particular condition that exposes it.

\-----------------------------------------------------------------------------------------------------------------------------------------------------------



**B. DEFECT CAUSES**



* Why does software have defects?

Software defects don't appear randomly. They usually originate from problems during different stages of development.

**1. Human Mistakes:** Software is created by humans, so mistakes can happen.

Misunderstanding a requirement

Typing incorrect code

Using the wrong variable

Incorrect calculation

Forgetting a condition

Copy-paste mistake

Incorrect configuration



**2. Requirement Problems:** Sometimes the problem starts before development even begins.

**Common requirement problems:**

Missing requirements

Ambiguous requirements (Confusing Requirements)

Incorrect requirements

Conflicting requirements

Incomplete requirements

Frequently changing requirements



**3. Design / Development Problems:** Even when requirements are correct, defects can be introduced during design or coding.

**Design problem:** Requirement: A user can have multiple delivery addresses.

But the database design allows only: User → One Address

Here, The design doesn't support the requirement.

**Development problem:** The design is correct, but the developer implements it incorrectly.

For example:

Expected: 1000 × 18% = 180

Developer writes code equivalent to: 1000 × 8% = 80

\--------------------------------------------------------------------------------------------------------



**C. DEFECT ECONOMICS**



Now we come to an important real-world concept -- **Cost of Fixing Defects!**

A defect generally becomes more expensive to fix when it is discovered later in the software lifecycle.

For example:

Requirement Stage

&#x20;     ↓

Design Stage

&#x20;     ↓

Development Stage

&#x20;     ↓

Testing Stage

&#x20;     ↓

Production



If a requirement problem is identified during requirement analysis, it can usually be clarified before significant development work is built around it.

But if the same problem reaches production, fixing it may involve:

* Code changes
* Database changes
* Testing
* Deployment
* Rollback/recovery
* Customer support
* Data correction



Hence, the overall cost and impact can be much higher.



**Example:**

Imagine a banking application has this requirement:

Daily withdrawal limit = **₹50,000.**

But the requirement was misunderstood and the system is designed around: **₹5,00,000.**



If discovered during **requirements**, **Simply clarify the requirement.**

If discovered during **development, Change the implementation.**

If discovered during **testing,** **Fix the code and retest.**

But, If discovered in **production,**

Now you may also have:

* Customer impact
* Financial risk
* Emergency fix
* Production deployment
* Additional regression testing
* Support effort



That's why organizations emphasize, **Early defect detection.**

The exact cost of Late Defect Detection depends on the project, defect, architecture, process, and organization.

**---------------------------------------------------------------------------------------------------------------------------------------------------------------------------**



**D. VERIFICATION \& VALIDATION**

Now we'll move to an extremely important testing concept.



**1. Verification:**

Verification answers: **Are we building the product correctly?**

Verification can involve activities such as:

* Requirement reviews
* Design reviews
* Code reviews
* Document reviews
* Static analysis

**Verification does not necessarily require executing the software.**



**Example**

**Requirement:** Password must contain at least 8 characters.

Developer's design/documentation says: Password minimum length = 6.

Before the application even runs, we can identify the inconsistency during review.

**That's verification.**



**2. Validation**

Validation answers**: Are we building the right product?**

It focuses on evaluating the actual software/product to determine whether it meets user/business needs and intended use.

**Testing the running application is a major part of validation.**



**Example:**

Requirement: User should be able to log in using valid credentials.

You run the application.

You enter: Valid email + Valid password, But login fails.

The product isn't behaving as expected.

**Testing has identified a problem during validation.**



* **Verification vs Validation**

**--------------------------------------------------------------------------------------------------------------------------------------------------------------------------**

**| 				Verification                            	| 				Validation                                      	|**

**| ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |**

**| Checks work products against specifications 	| Evaluates  actual product against intended needs 	|**

**| "Are we building the product correctly?"          	| "Are we building the right product?"                  		|**

**| Often involves reviews/inspections          		| Often involves executing/testing the software       	|**

**| Can be performed without executing software 	| Commonly involves execution of the product          	|**

**--------------------------------------------------------------------------------------------------------------------------------------------------------------------------**



Remember these two questions:

VERIFICATION: **"Are we building the product correctly?"**

VALIDATION: **"Are we building the right product?"**



* **Practical Example — ATM**

Requirement: ATM should allow a customer to withdraw cash after entering a valid card and PIN.

1. **Verification** :

Review the requirement/design:

**Valid card + Valid PIN + Sufficient balance**

&#x20;       		**↓**

**Cash withdrawal should be allowed**



**Verification** checks whether the design/specification correctly represents this requirement.

No ATM execution to withdraw money is necessary for this review.



**2. Validation:**

Actually use the ATM/application:

**Insert valid card → Enter valid PIN → Select withdrawal → Enter amount → Receive cash**

Here, we're checking whether the actual product behaves as intended.

**That's validation.**

**--------------------------------------------------------------------------------------------------------------------------------------------------------------------------**



**E. Software Quality, QA vs QC**



1. **What is Software Quality?
Software Quality** is the degree to which a software product meets its specified requirements and satisfies the needs and expectations for which it was intended.
In simpler terms:
**Good-quality software does what it is supposed to do, reliably and appropriately for its intended users.**
Quality is not just "the software has no bugs"
**For example, imagine a banking application:**
Login works correctly ✅
Money transfer works correctly ✅
Balance calculation is correct ✅
Application is extremely slow ❌
User cannot understand error messages ❌
The application may have correct functionality but still have quality problems.

**\* What can contribute to software quality?**
Depending on the product and requirements, quality can involve things such as:
**a. Functional Correctness:** Does it perform the required functions?

&#x09;i.e. Transfer ₹10,000 → ₹10,000 should be transferred.
	**b. Reliability:** Does it continue to work consistently?

&#x09;i.e. Application should not randomly fail during transactions.

&#x09;**c. Performance:** Does it respond within the required time?

&#x09;i.e. Search results should load within the specifies response time.

&#x09;**d. Usability:** Can users understand and use the application effectively?

&#x09;**e. Security:** Does the application protect data and prevent unauthorized access?

&#x09;**f. Maintainability:** Can the software be modified and maintained effectively.



**Example:**

Suppose an e-commerce application has this requirement:

**A customer should be able to place an order using a valid credit card.**

You test it and discover: Valid card **→** Payment successful **→** Order created

**Functionally, this is working.**

But suppose the payment page takes 3 minutes to respond.

**The functionality works, but the application may still have a quality problem related to performance.**

This is why:

**Software quality is broader than simply "no bugs."**



**2.	Quality Assurance (QA) vs Quality Control (QC)**

&#x09;The first thing to understand: **QA and QC are not the same thing.**



* **Quality Assurance — QA**

&#x09;Quality Assurance is focused on the processes and activities which are used to prevent defects and improve the way 	software is developed.

&#x09;**QA = Process-oriented,** It answers- **"Are we following a good process to build quality software?"**



**It involves:**

*Defining development/testing processes*

*Establishing standards*

*Process reviews*

*Code review practices*

*Test process improvement*

*Process audits*

*Preventive activities*

**So, QA is primarily about preventing problems and improving the process.**



* **Quality Control — QC**

&#x09;Quality Control is focused in evaluating the actual product to identify defects and determine whether it meets the 	required quality criteria.

&#x09;**QC = Product-oriented.** It answers- **"Does the actual product meet the required quality?"**



**It involves:**

*Executing test cases*

*Functional testing*

*Finding defects*

*Retesting*

*Regression testing*

*Inspecting the actual product*

**Software testing is generally considered an important quality control activity.**



**--------------------------------------------------------------------------------------------------------------------------**

**| 		Quality Assurance                  | 		Quality Control             	|**

**| ------------------------------------------------------------ | ---------------------------------------------------- |**

**| Process-oriented                    		| Product-oriented                		|**

**| Focuses on prevention               		| Focuses on detection            	|**

**| Improves development processes      | Evaluates developed product	|**

**| Preventive in nature                		| Corrective/detective in nature  	|**

**| Example: defining testing standards 	| Example: executing tests        	|**

**--------------------------------------------------------------------------------------------------------------------------**



**Real-World Example QA vs QC:**

Imagine your organization repeatedly releases applications with login defects.



* **QA approach**

Instead of simply finding the same login defects repeatedly, the organization investigates the process.

Maybe:

* *Requirements aren't reviewed properly.*
* *Developers don't perform code reviews.*
* *Test cases aren't reviewed.*
* *Acceptance criteria aren't clear.*



The organization improves the process. **That's Quality Assurance.**



* **QC approach**

The tester executes login tests and discovers: Valid users cannot log in.

Testing team reports the Defect. **That's Quality Control.**

**=============================================================================**



* **PRACTICAL EXERCISE — Verification vs Validation**

Classify each as primarily Verification or Validation.



1\. Tester executes the login application with valid credentials. - **Validation**

2\. Developer reviews another developer's code. - **Verification**

3\. QA reviews the requirement document for missing acceptance criteria. - **Verification**

4\. Tester enters an incorrect password and verifies the error message. - **Validation**

5\. Team reviews the database design against the requirements before implementation. - **Verification**



* **ASSIGNMENT:**

**Part A — Defect Terminology**



Q1. Using one example of your own, explain the difference between: Error → Defect → Failure

**ANS:** In an banking application, Requirement is: After adding a beneficiary account, customer can transfer money after 24 hrs.

Developer, mistakenly implements 42 hrs instead of 24 hrs.

Now, this mistake of developer leads to an error and remain in system.

Now, this error leads to the defect after implementing the functionality.

And this defect then leads to the failure of functionality when user is unable to transfer the money even after 24 hrs. The expected behaviour of functionality mismatches with actual behaviour.



**REVIEW:**

**Your example is good:** 

Requirement: Transfer should be allowed after 24 hours. Developer implements 42 hours.

Your overall chain is correct, but there is one terminology issue in how you described it.

**You wrote: "This mistake of developer leads to an error..."**

**Actually:**

**The developer's mistake itself is the Error.**

That error results in an incorrect implementation.

The incorrect implementation is the **Defect**.

When the defect is triggered during execution and produces incorrect behavior, that's the **Failure**.



Q2. Is a bug different from a defect?

**Ans:** No, Bug is just an another term that can be used interchangeably to that of defect.



Q3. Can a defect exist without immediately causing a failure? Explain briefly.

**Ans:** Yes. Because, defect does not always leads to failure. Failure happens only when a defect is executed in a certain condition and not every time.

Let's understand this with an example:

Requirement is: After adding a beneficiary account, customer can transfer money after 24 hrs.

Developer, mistakenly implements 42 hrs instead of 24 hrs.

Now, this mistake of developer leads to an error and remain in system.

Now, this error leads to the defect after implementing the functionality.

Now, an user adds the beneficiary but he does not have any urgency to transfer the money. He transfers the money after 72 hrs. 

And hence even the defect exist in the system, since the money is transferred after 42 hrs, the failure does not occur.

So, the failure occurs only if the defect is executed in a certain conditions.



**REVIEW:**

**Your answer is correct, and this is actually an important concept.**

One small wording improvement.

Instead of: "failure occurs only if the defect is executed in a certain condition"

say: **A failure occurs when the software executes under a condition that exposes the defect and produces incorrect behavior.**



**Part B — Defect Causes**

Classify each: Human mistake / Requirement problem / Design-development problem



Q4. The requirement says "fast response," but doesn't specify how fast. - **Requirement problem (Ambiguous requirement)** 

Q5. A developer accidentally writes 100 instead of 1000. - **Human Mistake**

Q6. The requirement clearly says users can have multiple addresses, but the database design supports only one. - **Design Problem**



**Part C — Defect Economics**

Q7. Why is finding a defect during requirement analysis generally better than finding it after production release?

**ANS:** Well, if a defect is found during Requirement Analysis then we just have to clarify the requirement before implementation. That's it. No extra time, effort and cost is required. 

If its found in production release, then it requires lot of efforts, would incur cost of retesting, changes in development (code), Design, we have to test it again after making changes in development, executing the features.

Hence, early defect detection is always better, cost and time saving than finding the defect in production stage.



**REVIEW:**

Your answer correctly identifies:

* Additional development effort
* Retesting
* Regression/testing effort
* Time
* Cost
* Production impact
* One important refinement



But one slight improvement. You said:

"No extra time, effort and cost is required."

I'd avoid saying no cost at all. Because, even requirement clarification consumes some time and effort.



**Better:**

**The cost and effort are generally much lower because the problem can be corrected before significant development and testing work has been built around it.**



**Part D — Verification \& Validation**

Q8. What is verification?

**Ans:** Verification answers - Are we building the product in right way?

It involves the work product conforms against the specified requirements and does not include execution of software.

verification checks whether the design/specification correctly represent the requirement.



**REVIEW:**

**Almost Correct, One refinement**

You said: "does not include execution of software."

For our foundation-level understanding, that's fine. But don't turn it into an absolute rule in interviews.



**A safer statement is:**

**Verification primarily involves reviewing or evaluating work products against specified requirements and can often be performed without executing the software.**



Q9. What is validation?

**Ans:** Validation answers - Are we building the right product?

Validation ensures that the actual product behaves as intended. It usually involves the execution of the software, functionality.



**REVIEW:**

**✅ Correct.** Your connection to software execution/testing is also correct.

But a clean interview version would be:

**Validation evaluates the actual software to determine whether it meets the intended requirements and user/business needs. It commonly involves executing and testing the software.**



Q10. Explain the difference between:

"Are we building the product correctly?" and "Are we building the right product?"

**Ans:** "Are we building the product correctly?" It basically means checking whether the product we are building is correctly representing the requirements. It involves reviews and inspection and done before actually building the prpoduct.

"Are we building the right product?" basically means  Evaluating the actual product against intended needs. It involves execution  or testing of software.



**REVIEW:**

Your answer is **correct**. You have understood the fundamental distinction.

One wording correction

You wrote: "Verification is done before actually building the product."

Don't always say this.

Verification activities can happen at different stages of development, not only before the product is built.

**Better:**

**Verification evaluates work products against specified requirements, while validation evaluates the actual product to determine whether it satisfies its intended needs.**

\-------------------------------------------------------------------------------------------------------------------------



**🔑 What You Should Remember From Group 2**



* **Defect terminology**

**Human mistake** **→** **ERROR** **→** **Incorrect implementation** **→** **DEFECT**  **→** **exposing defect at certain conditions** Leads to **FAILURE**



* **Defect causes**
1. Requirement Problem: Ambiguous / Missing / Conflicting requirement
2. Human Mistake: Person makes incorrect decision/action
3. Design / Development Problem: Incorrect design or implementation



* **Defect economics**

Earlier detection **→** Generally lower cost + lower impact

Later detection **→** Generally higher cost + higher impact



* **QA vs QC**

**QUALITY ASSURANCE**

PROCESS Oriented → Prevent defects (Improve how software is developed)

**QUALITY CONTROL** 

PRODUCT Oriented→ Detect defects (Evaluate the actual software)



* **Verification vs Validation**

**VERIFICATION**

"Are we building the product correctly?" **→** Check work products against requirements

**VALIDATION**

"Are we building the right product?" **→** Evaluate actual product against intended needs

**IMPORTANT**

QA improves the process to help prevent defects.
QC evaluates the product to detect defects.
Verification checks whether work products are built correctly against specifications.
Validation checks whether the actual product meets its intended needs.

================================================================================

