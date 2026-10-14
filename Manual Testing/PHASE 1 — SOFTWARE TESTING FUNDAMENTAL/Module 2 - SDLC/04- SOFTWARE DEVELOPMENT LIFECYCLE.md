###### **04- SOFTWARE DEVELOPMENT LIFECYCLE**



**1. WHAT IS SDLC?**

SDLC stands for Software Development Life Cycle.

SDLC is the process of delivering a high quality software to the end users through a series of steps from an initial idea/requirement until the software is deployed and maintained at the lowest cost and in the shortest time possible.

This is the process where “Software is built from idea to a real product and it does not stop at just software production, it goes beyond and takes care of the maintenance of the software as well.



* **Why do we need SDLC?**

Without a defined process, a project can become chaotic.

SDLC provides a structured approach:

* &#x09;Clear planning
* &#x09;Defined roles and responsibilities
* &#x09;Better communication between teams
* &#x09;Predictable timelines
* &#x09;Higher software quality
* &#x09;Reduced project risk



This approach helps businesses manage timelines, control costs, improve collaboration, and deliver reliable, high quality products through a repeatable and measurable development process.



Each organization may have its own process but they all follow the same pattern as involved in SDLC as a standard framework instead of unorganised development as below:



🔄 Phases of SDLC

Requirement ➥ Design ➥ Development ➥ Testing ➥ Deployment ➥ Maintenance



* Let's understand SDLC with an example:

Development of a Food Delivery Application where users can browse restaurants, place orders, make payments, and track deliveries.



1. **REQUIREMENT**: 

&#x20;Objective: *To understand what the client wants and what an user can expect (Requirements).*

The team tries to understand: *What problem are we solving, and what should the software provide?*



* At this stage, detailed functional and technical requirements are gathered from stakeholders.

**✅ Functional Requirements:** 

**For user:** User login, Search restaurants and menu, order food, Live order tracking, Online payment, Ratings \& reviews. 

**For Restaurant:** Restaurant onboarding, Menu management, Accept/reject orders

**For Rider:** Rider tracking, Earnings dashboard



**✅ Technical 0r Non-Functional Requirements:**

**App Load management:** App should support 1 lakh users 

**Performance:** App should load in 2 seconds, Order placement should happen within 2 seconds, 99.9% uptime

Secure payment transactions

App should work on across OS i.e. Android + iPhone



* BA/Development teams document user expectations, system specifications and other important aspects.

**📄 Documents Created:** Business analysts gather and document these requirements as below:

**BRD (Business Requirement Document):** A clear list of what business wants from the system (Business Goals)

**SRS (Software Requirement Specification):** Detailed technical and functional requirements.

**User Stories**



* This ensures the clarity of project development even before the design begins as a well defined requirement phase strengthens the whole SDLC process.



**🧠 QA Involvement:**

Many beginners think QA starts only in Testing phase, but in modern SDLC "Shift Left" approach is used which ensures the product quality, reducing the risk and saving time \& cost.



A tester can participate during requirements by:

\- Reviewing requirements

\- Identifying ambiguity

\- Identifying missing information

\- Checking whether requirements are testable

\- Identifying potential risks



For example:

Requirement: "The application should respond quickly."

Tester asks: "What response time is considered acceptable?"

**That's valuable testing involvement before coding even starts.**

\-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



**2.	DESIGN:**

**🎯 Objective:** *Convert requirements into technical blueprint.*



The design phase determines the technical and functional structure of the application.

🎨 **UI/UX designers** **develop**: User Interface, Mobile app screens, User flow, Prototypes

⚙️ **Development team define** s/m Architecture, **Design**: Frontend, Backend, Cloud, database

🔐 **Security Teams Design:** Security design decisions such as authentication mechanisms, password storage standards, authorization rules, API security, and encryption approaches are defined.



**📄 Documents Created:**

* **HLD (High Level Design):** Overall system architecture.
* **LLD (Low Level Design):** Detailed module-level design.
* **UI mockups:** Screen Designs



🧠 **QA Involvement:**

\- QA reviews: UI flows, Business flows, Design consistency

\- Validates if requirements are fulfilled/covered in design

\- QA may identify: Difficult-to-test flows, Missing validations, Usability issues

Finding design issues at this stage is much cheaper than after development.



A tester can review designs and ask questions such as:

* What happens if the payment service is unavailable?
* What happens if the database is temporarily unavailable?
* How will unauthorized access be prevented?

Again, the tester isn't waiting until the application is finished.



**Design ensures scalability and usability even before coding begins strengthens the SDLC by creating a blueprint for the project.**

\-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



**3.	DEVELOPMENT:**

**🎯 Goal:** *Actual coding begins and this is where developers build the product.*

**This is where developers implement the software according to the requirements and design.**



**Developers write:**

*- Application code*

*- APIs*

*- Database logic*

*- UI*

*- Business logic*

*- Integrations*



Developers work and write code feature-by-feature. Usually in Agile sprints:

&#x09;Sprint 1 → Login

&#x09;Sprint 2 → Restaurant API

&#x09;Sprint 3 → Cart \& Orders



**- Version Control:** Developers use GitHub/GitLab/Bitbucket and works in branches like feature/login and feature/payment

**-  Unit Testing:** Developers test their own code before handing it over to the testing environments.



**📄 Documents created/ Outcome:**

**- Source Code:** Actual code that builds the software

**- Build/Application package:** Executable version of the application



**⚠️ Real Problems at this phase:**

This phase has MOST chaos. Common issues include:

&#x09;- Code merge conflicts

&#x09;- Build failures

&#x09;- Environment issues

&#x09;- Dependency problems

&#x09;- Delayed features



🧠 **QA Involvement** :

\- Review implemented features against requirements before beginning formal testing.

\- Prepare detailed test scenarios, test cases and test data

\- Prepare RTM (Requirement Traceability Matrix)

\- Review builds received from developers

\- Sometimes QA also starts: API testing and Automation Planning (If Applicable)

By the time development is complete, QA is ready to start testing immediately.

\-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



**4.	TESTING:**

**🎯 Goal:** The developed software is evaluated against its requirements and expected behavior to ensure product quality before release.



At this stage, QA becomes heavily involved, They:

* *Execute tests*
* *Compare expected vs actual behavior*
* *Identify defects*
* *Prepare test execution reports.*
* *Log defects*
* *Retest fixes*
* *Provide quality metrics*
* *Perform regression testing*



And to achieve this, QA performs various types of testing such as:

* &#x09;*Functional testing*
* &#x09;*Regression testing*
* &#x09;*Integration testing*
* &#x09;*UI testing*
* &#x09;*Compatibility testing*
* &#x09;*Sanity testing*



**📄 Documents Created:**

* Test Summary report
* Defect reports: List of identified bugs/defects
* Test Cases Document

Example:

&#x09;Scenario		Expected Result

&#x09;1. Valid OTP	Login success

&#x09;2.Invalid OTP	Error message



* **Example:**

**Requirement**: Valid user should be able to log in.

Tester executes the application:

Valid email + Valid password

&#x20;               Login

Expected: Login Successful

Actual: Application displays- "Invalid credentials" (Login Rejected)



This is the potential defect, QA logs a defect with clear reproduction steps and evidence.

QA then provides testing sign-off or recommends release based on testing results.

The final release approval is generally a business decision involving Product Owner, Release Manager, or stakeholders.

\-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



**5.	DEPLOYMENT**

**🎯 Goal:** Release the working software to users



Once the software has met the necessary release criteria, it can be deployed to the target environment step by step  such as:

* Development
* QA Environment
* UAT Environment
* Staging
* Production



**Deployment means making the software available in the environment where it is intended to operate.**



**📄 Documents created/ Outcome:**

Release notes: details of features and fixes released

Production environment: Live platform/System accessible to customers



🧠 **QA Involvement** :

Depending on the organization, testers may participate in:

\- Release validation

\- Smoke/sanity checks

&#x09;QA Verifies the deployed application through Smoke testing to ensure critical functionality works in the target 	environment.

\- Production verification

\- Deployment verification

\- Confirming critical functionality works after deployment



For example: Typical checks:

* Can user log in?
* can core features be accessed?
* Are integrations functioning well?
* Is the application stable?

\-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



**6.	MAINTENANCE:**

**🎯Objective:** Ensure the product runs smoothly after release



Software development doesn't end after deployment. Once users start using the application, things can change.

For example:

\- Bugs are discovered and reported by users

\- New features are requested

\- Business rules change

\- Security updates are needed

\- Performance improvements are required

\- Technology changes

\- Regulations change

**Therefore, software enters the maintenance phase. It helps software evolve continuously.**



🧠 **QA Involvement** :

Bug verification

Regression testing for changes

Testing enhancements

Validation hotfixes

Ensuring existing functionality remains unaffected



**Example**

Banking application is already live.

Business says: "We now need UPI payments."

The team modifies the existing system.

Or users report: "Statement download fails for some accounts."

The team investigates and fixes the issue. 

Thus, Testing is required again for the changes/improvements made.

============================================================================



* **Where Does the Tester Fit in SDLC?**



As per SDLC flow, common beginner misconception is that QA role best fits at Testing stage once development finishes. But in practicality and in Modern SDLC process, A strong QA Engineer:

\- Starts participating from the requirement gathering phase

\- Looks for the possible risks and defects in requirements and design, not just in the product/Software

\- Thinks proactively about risks and edge cases.

\- Understand the business domain before writing the test cases.

\- Collaborates with BAs, developers, product owners, and Devops teams throughout the SDLC.



**Remember,** *the earlier a defect is found, the cheaper and easier it is to fix.*

**QA is not just "testing.", QA is preventing defects before they are built.**

**======================================================================**



**ASSIGNMENT**

Imagine you're part of a team building a Banking Application.

The application needs:

\- Login

\- Account balance

\- Beneficiary management

\- Money transfer

\- Statement download



Part A

Explain what would happen during each SDLC phase:

1\. Requirements- What would the team determine?

The team determines:

What the application should do?

Review the requirements

Functional and Technical requirements are determined

**Functional Requirements:** 

Login: Exactly how login works (e.g., biometrics, OTP, passwords, PIN, etc)

Account Balance: Is there a need to login or enter the PIN again to check account balance?

Beneficiary management: What is the TAT to add the beneficiary? Is there a different criteria, after effects for Same Bank beneficiary and different bank beneficiary? 

Money Transfer: Transaction limits for money transfers, Can money be transferred to the beneficiary immediately?

Modes of transfer?

Bank Statement: How statement is downloaded? Via Emial or direct? How far back a statement download can go?



Non-Functional: Regulatory requirements like KYC (Know Your Customer), data encryption standards, and multi-factor authentication (MFA), what platforms does the application support- iOS, Android, WEB?



BAs would prepare the BRD and SRS documents

QAs would look for missing requirements, ambiguities, etc.



2\. Design- What would the team decide?

This phase transforms requirements into blueprints. The team would decide:

**System Architecture:** How the frontend (user interface) will securely talk to the backend servers and the core banking database.

**Database Design:** The structure of data tables (e.g., Users, Accounts, Transactions, Beneficiaries) and how they link together.

**UI/UX Layout:** The visual wireframes and user flows showing how a customer navigates from the login screen to sending money.



3\. Development- What would developers do?

This is the coding phase. Developers split up the tasks and write the actual software:

Developers would write the code according to the requirements. They would write code functionality wise and use Version control like Github to push the code on server.

They write codes for frontend, backend and  secure APIs to process money transfer, etc.



4\. Testing What would testers do?

Testers ensure the application is secure, reliable, and works exactly as intended:

• Functional Testing: Verifying that money is correctly deducted from the sender and added to the beneficiary during a transfer.

• Security \& Penetration Testing: Trying to "hack" the app to find vulnerabilities in the login system or data leaks in the statement downloads.

• Performance Testing: Checking if the system can handle thousands of users checking their account balances simultaneously on payday without crashing.



5\. Deployment What would happen?

This is the launch phase where the application is pushed to production:

• App Store Submission: Releasing the mobile versions to the Apple App Store and Google Play Store.

• Server Setup: Deploying the backend code to live cloud servers or the bank's secure data centers.

• Data Migration \& Monitoring: Setting up initial databases and activating real-time monitoring tools to watch for crashes or server overload immediately after launch.



6\. Maintenance What could happen after release?

Once the app is live, the team enters a cycle of ongoing support and updates:

• Bug Fixes: Resolving unexpected glitches that real users encounter (e.g., a specific phone model crashing during statement downloads).

• Security Patches: Updating the app to defend against newly discovered cyber threats.

• Feature Updates: Adding new capabilities based on user feedback, such as adding a "Dark Mode" or supporting new payment methods.

\------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



Q1. What is SDLC?

Ans: SDLC stands for Software Development LifeCycle.

It is a structured process where various teams collaborate to develop and deliver a high quality software within the shortest possible time and at lowest capital.



Q2. Why is SDLC important?

Well, SDLC is important because without a structured process Software development can become chaotic and there would be high chances of producing a Low Quality Product.

SDLCs structured flow ensures collaboration between various teams which leads to producing a quality product.



Q3. What are the phases of SDLC? Explain what happens at each stage.

There are basically 6 phases in SDLC namely-

* Requirement gathering and Analysis
* Design
* Development
* Testing
* Deployment
* Maintenance





Q4. What happens during the requirement phase?

During this phase, stakeholders, project managers, and business analysts gather, analyze, and document what the software needs to do. They define the functional features, security requirements, and hardware/software constraints, which are compiled into a Software Requirement Specification (SRS) document.



Q5. What is the purpose of the design phase?

The purpose of the design phase is to transform requirements into technical blueprints. 

The team decides on the system architecture, database structure, user interface (UI/UX) layouts, and third-party integrations before any actual coding begins.



Q6. What happens during development?

During development, programmers write the actual source code based on the design blueprints. They build the database systems, create frontend interfaces, develop backend logic, and run initial code checks (unit testing) to build the operational software.



Q7. What is the role of testing in SDLC?

The role of testing is to verify that the software works correctly and securely. Testers find, log, and track bugs, ensure the application matches the original requirements, and evaluate performance to guarantee a smooth user experience.





Q8. What is deployment?

Deployment is the phase where the finalized software is released into the production environment and made available to actual users. This includes publishing apps to app stores, setting up live cloud servers, and configuring databases.



Q9. Does SDLC end after deployment? Why?

No, SDLC does not end after deployment. It moves into the maintenance phase. Software requires continuous monitoring because real-world use reveals hidden bugs, operating systems update (requiring compatibility patches), and user needs evolve over time.



Q10. Can a tester be involved during the requirement phase?

Yes, testers can and absolutely should be involved during the requirement phase. Their early involvement is a core practice in modern software methodologies like Agile and DevOps.

QAs getting involved as early as possible in SDLC process could lower the risk of potentail software failure, saves time and cost relatively.



Q11. Why should a tester be involved early in SDLC?

• Prevents requirement defects: Testers identify vague, contradictory, or untestable requirements before coding starts.

• Reduces fixing costs: Finding a flaw in a text document is drastically cheaper than fixing a flaw buried deep inside written code.

• Enables early test planning: It allows testers to design test strategies and test cases well ahead of schedule, accelerating the overall timeline.



Q12. What can a tester do during the maintenance phase?

• Regression Testing: Verifying that new bug fixes or feature updates haven't accidentally broken existing parts of the application.

• User Feedback Validation: Testing specific scenarios reported by real clients to help replicate and pinpoint production bugs.

• Upgrade Testing: Checking the application's stability when upgrading underlying servers, databases, or third-party tools.

=============================================================================

