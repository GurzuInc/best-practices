
# Bug Reporting Template

  

#### <span style="font-weight: 400;">Who can report Defect/Bug?</span>

  

<span style="font-weight: 400;">Anyone came across the bug can report bug/defect and put that on the Project/Product Backlog.</span>

  

<span style="font-weight: 400;">After reporting the Bug QA team can organize the Triage meeting to set the priority and severity of that bug. Development Team lead, QA Team lead and Project Manager decide in which sprint that bug will be fix or that bug needs to be hotfix.</span>

  

<span style="font-weight: 400;">**Note:** If any team member other than QA found the bug/defect they have to assign that bug/defect to the QA of their project to verify whether that is bug/defect or not. </span>

  

---

  

### <span style="font-weight: 400;">Template</span>

  

<span style="font-weight: 400;">---------------------------------------</span>

  

#### <span style="font-weight: 400;">Bug Title </span>

  

<span style="font-weight: 400;">A bug title is read more frequently than any other part of the bug report and should be clear and concise.</span>

  

<span style="font-weight: 400;">Everybody should be able to determine what the bug is without having to open the entire report.</span>

  

#### <span style="font-weight: 400;">Description</span>

  

<span style="font-weight: 400;">A well-defined bug description allows for an easy understanding of the bug and what happens.</span>

  

#### <span style="font-weight: 400;">Platform/Environment/Version/Context</span>

  

<span style="font-weight: 400;">It is also essential to include what operating system, browser configurations, and versions are being utilized when the bug is present.</span>

  

#### <span style="font-weight: 400;">Roles</span>

  

<span style="font-weight: 400;">Mention the in which user the bug has been replicated. (User roles)</span>

  

#### <span style="font-weight: 400;">Step to Reproduce</span>

  

<span style="font-weight: 400;">This provides clear instructions on how the bug can be reproduced by your developers.</span>

  

#### <span style="font-weight: 400;">Expected Results</span>

  

<span style="font-weight: 400;">Mention what is the expected results</span>

  

#### <span style="font-weight: 400;">Actual Results</span>

  

<span style="font-weight: 400;">Mention what is actually happening currently in that bug </span>

  

#### <span style="font-weight: 400;">Screenshot / Attachments / Screen Recording</span>

  

<span style="font-weight: 400;">Include a clear screenshot at the point of failure and when the bug occurred.</span>

  

---

  

#### <span style="font-weight: 400;">Example</span>

  

[![image-1626092642546.png](Images\Screenshots-Example.png)

  

Fig: Bug Example

  

<div id="bkmrk--2"><div><div></div></div><svg class="SnapLinksHighlighter" xmlns="http://www.w3.org/2000/svg"> </svg></div>

  

# Task Filing Template

  

### <span style="font-weight: 400;">Task Title </span>

  

<span style="font-weight: 400;">Task Title must be clear and concise. Any user can understand the task by just reading the task title.</span>

  

### <span style="font-weight: 400;">Description</span>

  

<span style="font-weight: 400;">A well-defined task description allows for an easy understanding of the task.</span>

  

### <span style="font-weight: 400;">Acceptance Criteria ([AC](https://www.altexsoft.com/blog/business/acceptance-criteria-purposes-formats-and-best-practices/))</span>

  

<span style="font-weight: 400;">Acceptance Criteria are the conditions that a software product must meet to be accepted by a user, a customer, or the system.</span>

  

<span style="font-weight: 400;">AC can be written in different formats. There are two most common ones, and the third option is to devise your own format:</span>

  

- **Scenario-oriented (Given/When/And/Then):**

  

<span style="font-weight: 400;">The scenario-oriented format is the acceptance criteria type that comes in the scenario form and illustrates each criterion.This approach was inherited from behavior-driven development(BDD) and provides a consistent structure that helps testers define when to begin and end testing a particular feature. It also reduces the time spent on writing test cases as the behavior of the system is described upfront.</span>

  

It is approached through the *Given/When/Then* (GWT) sequence that looks like this:

  

1. *Given* some precondition

2. *When* I do some action

3. *Then* I expect some result

  

The acceptance criteria template includes the following statements:

  

1. Scenario – the name for the behavior that will be described

2. Given – the beginning state of the scenario

3. When – specific action that the user makes

4. Then – the outcome of the action in “When”

5. And – used to continue any of three previous statements

  

Example:

  

**User Story:** As a user, I want to be able to recover the password to my account, so that I will be able to access my account in case I forgot the password.

  

**Scenario:** Forgot password

  

- **Given:** The user navigates to the login page

- **When**: The user selects &lt;*forgot password&gt;* option

- **And**: Enters a valid email to receive a link for password recovery

- **Then**: The system sends the link to the entered email

- **Given:** The user receives the link via the email

- **When:** The user navigates through the link received in the email

- **Then:** The system enables the user to set a new password

  

- **Rule-oriented (Checklist)**

  

The rule-oriented form entails that there is a set of rules that describe the behavior of a system. Based on these rules, we can draw specific scenarios.Usually, criteria composed using this form look like a simple bullet list.

  

<span style="font-weight: 400;">Example:</span>

  

**User story:** As a user, I want to use a search field to type a city, name, or street, so that I could find matching hotel options.

  

**Basic search interface acceptance criteria**

  

- The search field is placed on the top bar

- Search starts once the user clicks “Search”

- The field contains a placeholder with a grey-colored text: “Where are you going?”

- The placeholder disappears once the user starts typing

- Search is performed if a user types in a city, hotel name, street, or all combined

- Search is in English, French, German, and Ukrainian

- The user can’t type more than 200 symbols

- The search doesn’t support special symbols (characters). If the user has typed a special symbol, show the warning message: “Search input cannot contain special symbols.”

  

- **Custom formats**

  

We can invent our own acceptance criteria given they serve their purposes, are written clearly in plain English, and can't be misinterpreted.

  

**Example: Strong Password Acceptance Criteria**

  

<table border="1" id="bkmrk-data-expected-result" style="border-collapse: collapse; width: 100%; height: 261px;"><tbody><tr style="height: 29px; background-color: silver;"><td style="width: 33.3333%; height: 29px;">**Data**</td><td style="width: 33.3333%; height: 29px;">**Expected Result**</td><td style="width: 33.3333%; height: 29px;">**Expected Message**</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">Aa$5777</td><td style="width: 33.3333%; height: 29px;">Fail</td><td style="width: 33.3333%; height: 29px;">Too Short</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">AAbbDD11</td><td style="width: 33.3333%; height: 29px;">Fail</td><td style="width: 33.3333%; height: 29px;">No Specific Characters</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">$$$aaa111</td><td style="width: 33.3333%; height: 29px;">Fail</td><td style="width: 33.3333%; height: 29px;">No Upper Case</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">GGG$$$333</td><td style="width: 33.3333%; height: 29px;">Fail</td><td style="width: 33.3333%; height: 29px;">No Lower Case</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">SSS\*\*\*hhhhhh</td><td style="width: 33.3333%; height: 29px;">Fail</td><td style="width: 33.3333%; height: 29px;">No Numbers</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">CharcatersMoreThan11$$$</td><td style="width: 33.3333%; height: 29px;">Fail</td><td style="width: 33.3333%; height: 29px;">Max Password Length is 255</td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">This@ISGood11</td><td style="width: 33.3333%; height: 29px;">Pass</td><td style="width: 33.3333%; height: 29px;"> </td></tr><tr style="height: 29px;"><td style="width: 33.3333%; height: 29px;">P@ssword11%</td><td style="width: 33.3333%; height: 29px;">Pass</td><td style="width: 33.3333%; height: 29px;"> </td></tr></tbody></table>

  

### <span style="font-weight: 400;">Definition of Done ([DoD](https://www.leadingagile.com/2017/02/definition-of-done/))</span>

  

<span style="font-weight: 400;">The definition of done (DoD) is when all conditions, or acceptance criteria, that a software product must satisfy are met and ready to be accepted by a user, customer, team, or consuming system. It lowers rework, by preventing user stories that don’t meet the definition from being promoted to higher level environments. It will prevent features that don’t meet the definition from being delivered to the customer or user.</span>

  

##### <span style="font-weight: 400;">User Stories</span>

  

The most common use of DoD is on the delivery team level. Done on this level means the Product Owner reviewed and accepted the user story. Once accepted, the “done” user story will contribute to the team velocity.

  

**User Story DoD Examples:**

  

- Unit tests passed

- Code reviewed

- Acceptance criteria met

- Functional tests passed

- Non-Functional requirements met

- Product Owner accepts the User Story

  

##### Features

  

Done on this level means it qualifies to add to a release. Not all user stories need to be completed. Rather, it means the feature may be sufficient to satisfy the need. Once accepted, the done feature will contribute to the release velocity.

  

**Feature DoD Examples:**

  

- Acceptance criteria met

- Integrated into a clean build

- Promoted to higher level environment

- Automated regression tests pass

- Feature level functional tests passed

- Non-Functional requirements met

- Meets compliance requirements

- Functionality documented in necessary user user documentation

  

##### Epics

  

Done on this level refer to a organizational strategic priority, portfolio plan item, or some other collection of features that satisfied a market need. Not all user stories or features need to be completed. Rather, the epic is sufficient to satisfy the need. Once accepted, the done epic will contribute to throughput calculations to see if the supply is in balance with demand.

  

**Epic DoD Examples:**

  

- Non-Functional requirements met

- End-to-end integration completed

- Regression tests pass

- Promoted to production environment

- Meets defined market expectations

  

### <span style="font-weight: 400;">Design Mockup/wireframe as a Attachments</span>

  

<span style="font-weight: 400;">If needed the design mockup/wireframe must be attached for a better understanding of the task and the UI flow.Expected Message</span>

  

<div id="bkmrk-"><div><div></div></div><svg class="SnapLinksHighlighter" xmlns="http://www.w3.org/2000/svg"> </svg></div>

  

# Defect Tracking and Reporting Flow Chart

  

## <span style="font-weight: 400;">Defect Tracking and Reporting Flow chart</span>

  

<span style="font-weight: 400;">The following flowchart depicts Defect Tracking Process:</span>

  

[![image-1626085953602.png](Images\Defect-Tracking-and-Reporting-Flow-chart.png)

  

<span style="font-weight: 400;">Fig: defect tracking &amp; reporting flowchart</span>

  

## <span style="font-weight: 400;">Defect Severity</span>

  

<span style="font-weight: 400;">Defect found during the Testing will be categorized according to the bug-reporting tool and the categories are: </span>

  

<table border="1" id="bkmrk-severity-impact-colo" style="border-collapse: collapse; width: 100%;"><tbody><tr style="background-color: silver;"><td style="width: 11.7284%;">Severity</td><td style="width: 75.0617%;">Impact</td><td style="width: 13.2098%;">Color Code</td></tr><tr style="border-style: solid;"><td style="width: 11.7284%; height: 87px;"><span style="font-weight: 400;">1 (Critical)</span>

  

</td><td style="width: 75.0617%; height: 87px;">- <span style="font-weight: 400;">This bug is critical enough to crash the system, cause file corruption, or cause potential data loss</span>

- <span style="font-weight: 400;">It causes an abnormal return to the operating system (crash or a system failure message appears).</span>

- <span style="font-weight: 400;">It causes the application to hang and requires rebooting the system.</span>

  

</td><td style="width: 13.2098%; background-color: #d40000; height: 87px;"><span style="font-weight: 400;">\#d40000</span></td></tr><tr style="border-style: solid;"><td style="width: 11.7284%; height: 53px;"><span style="font-weight: 400;">2 (High)</span>

  

</td><td style="width: 75.0617%; height: 53px;">- <span style="font-weight: 400;">It causes a lack of vital program functionality with a workaround.</span>

  

</td><td style="width: 13.2098%; background-color: #ff6600; height: 53px;"><span style="font-weight: 400;">\#ff6600</span></td></tr><tr style="border-style: solid;"><td style="width: 11.7284%; height: 104px;"><span style="font-weight: 400;">3 (Medium)</span>

  

</td><td style="width: 75.0617%; height: 104px;">- <span style="font-weight: 400;">This Bug will degrade the quality of the system. However, there is an intelligent workaround for achieving the desired functionality - for example through another screen.</span>

- <span style="font-weight: 400;">This bug prevents other areas of the product from being tested. However other areas can be independently tested.</span>

  

</td><td style="width: 13.2098%; background-color: #ffd42a; height: 104px;"><span style="font-weight: 400;">\#ffd42a</span></td></tr><tr style="border-style: solid;"><td style="width: 11.7284%; height: 53px;"><span style="font-weight: 400;">4 (Low)</span>

  

</td><td style="width: 75.0617%; height: 53px;">- <span style="font-weight: 400;">There is an insufficient or unclear error message, which has a minimum impact on product use.</span>

  

</td><td style="width: 13.2098%; background-color: #ffeeaa; height: 53px;"><span style="font-weight: 400;">\#ffeeaa</span></td></tr><tr style="border-style: solid;"><td style="width: 11.7284%; height: 53px;"><span style="font-weight: 400;">5 (Cosmetic)</span>

  

</td><td style="width: 75.0617%; height: 53px;">- <span style="font-weight: 400;">There is an insufficient or unclear error message that has no impact on product use.</span>

  

</td><td style="width: 13.2098%; background-color: #ffaaaa; height: 53px;"><span style="font-weight: 400;">\#ffaaaa  

</span></td></tr></tbody></table>

  

##### References:

  

https://www.softwaretestinghelp.com/defect-reporting-habits/

  

<div id="bkmrk--0"><div><div></div></div><svg class="SnapLinksHighlighter" xmlns="http://www.w3.org/2000/svg"> </svg></div>

  

