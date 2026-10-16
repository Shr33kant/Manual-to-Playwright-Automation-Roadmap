###### **05 - SDLC MODELS**



This module is about understanding how software development is organized under different SDLC models and how a tester’s involvement changes in each model.



In SDLC we learned various phases involved-

Requirements → Design → Development → Testing → Deployment → Maintenance



Whereas SDLC model defines how these phases are organized, performed, and revisited during software development.

Different models use different approaches:

\- Some complete phases largely in sequence.

\- Some emphasize testing alongside development.

\- Others deliver software in small increments and adapt to feedback.



Lets-'s understand these models one by one.



1. **WATERFALL MODEL: The oldest and simplest of all.**

The Waterfall model follows a largely sequential approach, where one phase must be completed before the next begins.

Think of a waterfall: Water flows only downward, it never goes back up.

Similarly, in waterfall model as well, once a phase is completed, going back is difficult and expensive.



Suppose a bank commissions a fixed-scope application, and its requirements are well understood.



1\. Requirements - The team gathers and documents requirements.

2\. Design - Architects design the system.

3\. Development - Developers build the application.

4\. Testing - Testers test the completed build.

5\. Deployment - The application is deployed.

6\. Maintenance - The team maintains it after release.



**This is a simplified Waterfall flow. In practice, teams may revisit earlier phases when problems arise.**



**Advantages:**

* Simple and easy
* Clear documentation
* Well-defined milestones
* Suitable for stable requirements
* Easy project tracking



**Disadvantages:**

* Very difficult to accommodate changes in requirements
* Testing starts late only after the development finishes.
* Bugs are found late
* High cost of fixing defects
* Customer gets the access to the product very late, only at the end of project completion, hence the feedback is shared late, changes becomes difficult and expensive



**Tester involvement**

In a traditional Waterfall process, formal testing often happens after development.

However, testers do not necessarily remain idle until development finishes.

They can:

* Review requirements and design documents earlier
* Identify ambiguity
* Prepare test plans
* Develop test cases before a testable build is available.

**---------------------------------------------------------------------------------------------------------------------------------------------------------------**



**2. V - MODEL (Verification \& Validation Model)**

The V model improves upon Waterfall by integrating testing activities with every development phase.

It emphasizes testing as soon as development planning starts. Testing still occurs after coding, but QA is involved much earlier.



The left side is Verification and the right side is Validation. It makes the shape of "V" hence the name is "V Model.

Each testing level is planned in relation to a development or specification stage.



**VERIFICATION									   VALIDATION**

&#x09;  **↓											    ↓**

**Requirements						←→			Acceptance Testing**

Specification   									Checks user needs



**System Design					←→			System Testing**

Whole-system design							Checks full system



**Architecture / Integration Design		←→			Integration Testing**

Components and interfaces						Checks interactions



**Module / Detailed Design			←→			Unit Testing**

Individual components							Checks individual units

&#x09;							   **↓**

&#x09;					**Implementation / Coding**



**Example - For a banking application:**

\- When requirements are written, acceptance tests can be planned.

\- When system design is created, system tests can be planned.

\- When component interactions are designed, integration tests can be planned.

\- When detailed modules are designed, unit tests can be planned.



**The key idea is that testing is planned early, rather than being treated only as the final phase.**



**Tester involvement**

Even before the official testing phase begins, testers can:

* Review requirements and design documents
* Identify test conditions
* Prepare test cases early, and later execute the relevant tests when software becomes available.



**Advantages**

* Testing is planned early.
* Traceability between requirements and testing is clearer.
* Structured and useful for projects with stable requirements and strong documentation needs.



**Disadvantages:**

* Better than Waterfall but still difficult to handle changing requirements due to the Sequential process
* Expensive to modify completed phases
* Changes can require rework across related stages.
* Less flexible when requirements evolve frequently.
* Working software and feedback may arrive relatively late.

**---------------------------------------------------------------------------------------------------------------------------------------------------------------**



**3. AGILE MODEL: Agile is an iterative and incremental approach to software development.**

**Iterative:** Improving or refining something through repeated cycles.

**Incremental:** Add usable functionality in smaller pieces over time.



Agile was introduced because software projects needed to adapt to changing requirements which both Waterfall and 

V-model failed in.

Instead of building the whole product at once, the team delivers small working features in short cycles called as "Sprints".

A sprint usually lasts 1 to 4 weeks, most organization works in the sprint of 2 weeks.



Each sprint produces a working piece of software. 

Unlike the Waterfall and V-Model, customers see progress continuously and can provide feedback after each sprint which makes changes to be accommodate easily and also at low cost. 



**Workflow:**

Sprint Planning

&#x09;↓

Development

&#x09;↓

&#x20;   Testing

&#x09;↓

&#x20;   Review

&#x09;↓

&#x20;   Release

&#x09;↓

&#x20; Next Sprint



**Example A banking app team may develop features over successive iterations:**

* Iteration 1: Login
* Iteration 2: Account balance
* Iteration 3: Beneficiary management
* Iteration 4: Fund transfer



Each iteration can involve planning, design, development, testing, review, and potentially releasing the increment. 

The exact workflow depends on the team.



**Tester involvement**

In Agile, QA is a full team member and not someone who joins only after the development.

Testers collaborate throughout the iteration, not just at the end.

**They can:**

* Participate in Sprint Review and Retrospective.
* Review User Stories and Acceptance Criteria.
* Identify risks and clarify expected behavior.
* Prepare and execute tests as features are developed.
* Report defects and retest fixes.
* Perform regression testing to check existing functionality.
* Help the team assess whether a feature is ready.



**Automation is especially useful in Agile teams because repeated regression checks can be run frequently. But Agile does not mean everything must be automated.**



**Advantages**

* Adapts more readily to changing requirements.
* Provides frequent feedback.
* Delivers functionality in smaller increments.
* Encourages collaboration among developers, testers, and business stakeholders.



**Limitations**

* Requires regular communication and active collaboration.
* Poorly managed changes can lead to unclear scope.
* Insufficient regression testing can allow older features to break.
* Documentation still matters; Agile does not mean “no documentation.”

**---------------------------------------------------------------------------------------------------------------------------------------------------------------**



**Tester involvement: the main takeaway in each model**

**Waterfall**

Review and prepare early where possible; however formal execution commonly happens after development.



**V-Model**

Plan testing alongside specification and design; execute the corresponding test levels when the software is available.



**Agile**

Collaborate continuously, test within iterations, provide rapid feedback, and maintain regression coverage.



**Remember: the SDLC model influences when and how testing happens, but testers can contribute throughout the development lifecycle in every model.**

**================================================================================**



