# Sample Test Plan

### <span id="bkmrk--1" style="font-weight: normal;"><span style="border-width: initial; border-style: none; display: inline-block; overflow: hidden; width: 130px; height: 106px;">![](https://lh6.googleusercontent.com/Iln1Zv0Ixo6wOyqckh6FC6ARnqqi9lRuXQlJONyLluBFHsWM983fDgBQH1FFW0R3hD6ZFNSTO6FbSNf-sSo0j5vk9i0Gkwzh3b5L8TbAHwXiAU3XTOfPMHUxCGZ1MtnnC_CIwgaz)</span></span>

### Project Name

####   
Test Plan Document

  
MM-DD-YYYY  
Version: x.x.x  
Author: QA Engineer  
Reviewed by: Product Owner  
Revised Date: MM-DD-YYYY

##### Table of Contents

  
About document 2  
Scope of test 2  
Features to be tested 2  
Assumptions, Suspensions, and Resumptions 2  
Project Management Tool 2  
Test Management Tool 2  
Test Environment 3  
Tools Used 3  
Preliminary Action needs to be taken before Sprint 3  
Test to Perform 3  
Issue Logging (Defect Tracking and Reporting) 4  
Defect Severity 4  
Bug Reporting Template 5  
JIRA Task Template 5  
Test Completeness 5  
Test Deliverables 6  
Before Testing Phase 6  
During the Testing 6  
After the testing cycle is over 6  
Test Process 6  
Roles and Responsibilities 7  
Risks, Issues, and Dependencies 7  
List of Approvals 7  
Terms/Acronyms 8

#####  

#####   
About document

  
The document highlights the Quality Assurance process implemented for the Audit app of the Sunseeker hotel network. Once we plan for future releases, the test plan will be updated accordingly.

#####   
Scope of test

Test Scenarios/Test Objectives that will be validated. Clear picture for what we are going to cover (Example: Functional Test, Non-functional Test, etc).

#####   
Features to be tested

After the Sprint planning, the QA team will prepare all the required test data, Automated scripts, for the feature to be tested in the sprint.

##### Assumptions, Suspensions, and Resumptions

Sunseeker app will work on the attached link browser description. Browser compatibility is the most important at least the web application supports the below-mentioned browser.  
**Browser Support**: Chrome, Firefox, Safari, and Internet Explorer   
**Responsiveness**: Mobile Responsiveness

##### Project Management Tool

- JIRA for the Sprint cycle management
- Confluence for the track of the documents
- Figma for the Design

##### Test Management Tool

- JIRA for Bug/Defect Tracking
- Confluence to track the documents
- Google spreadsheet to handle the SOW (One pager).
- Google document to handle the Release notes, Diagnosis Report, etc.

##### Test Environment

- Web application (Chrome / Firefox / Safari)
- Development
- Android Smartphones for the Test in Android
- iPhone for the Mobile app test in the IOS
- Android Studio
- Virtual Machine for the Device compatibility

##### Tools Used

- Appium for Mobile App Testing
- JMeter for Non-functional Test
- Postman for the APIs testing
- Cypress for end to end Web app testing

##### Preliminary Action needs to be taken before Sprint

Before starting the Sprint all the team members should sit and have a Backlog Grooming session. By doing this Project Manager will communicate about the task to all the team members so that the QA team can fill all the Acceptance Criteria and the Definition of Done to the Description of the Task on JIRA.

##### Test to Perform

- Design mockup UI test.
- Perform the test case document.
- Review the test plan document.
- Branch-wise Feature test on the Development Environment (Server).
- Integrated Functional test on the QA Environment (Server) and use the tools for the better test report.
- Prepare the Test Coverage Report.
- Prepare a Release note and the Sprint User Manual.

##### Issue Logging (Defect Tracking and Reporting)

Issues will be logged using JIRA and depending upon the severity, the issue will be tracked in the backlog or assigned to the developer in the current sprint.

![Test Plan - Defect tracking and Reporting workflow.png](XDdkyEAgpMs4oDkr-test-plan-sandcastle.png)  
Fig: Defect tracking and Reporting workflow

##### Defect Severity

Defect found during the Testing will be categorized according to the bug-reporting tool and the Categories are:

<table border="1" id="bkmrk-severity-impact-1-%28c" style="border-collapse: collapse; width: 100%;"><tbody><tr><td style="width: 50%;">Severity</td><td style="width: 50%;">Impact</td></tr><tr><td style="width: 50%;">1 (Critical)</td><td style="width: 50%;">- This bug is critical enough to crash the system, cause file corruption, or cause potential data loss
- It causes an abnormal return to the operating system (crash or a system failure message appears).
- It causes the application to hang and requires rebooting the system.

</td></tr><tr><td style="width: 50%;">2 (High)</td><td style="width: 50%;">- It causes a lack of vital program functionality with a workaround.

</td></tr><tr><td style="width: 50%;">3 (Medium)</td><td style="width: 50%;">- This Bug will degrade the quality of the system. However, there is an intelligent workaround for achieving the desired functionality - for example through another screen.
- This bug prevents other areas of the product from being tested. However other areas can be independently tested.

</td></tr><tr><td style="width: 50%;">4 (Low)</td><td style="width: 50%;">- There is an insufficient or unclear error message, which has a minimum impact on product use.

</td></tr><tr><td style="width: 50%;">5 (Cosmetic)</td><td style="width: 50%;">- There is an insufficient or unclear error message that has no impact on product use.

</td></tr></tbody></table>

#####   
Bug Reporting Template

  
For the Bug Reporting Template Please follow the below-mentioned [link](https://docs.google.com/document/d/1Dnohx3NVnYApA9XNPiAE_CVG9sMFB2QK3H3piSpT5kc/edit).

##### JIRA Task Template

For the Task filing template please follow the below-mentioned [link](https://docs.google.com/document/d/1YpKUTu3YFFgVi_w2hWf1qC28DNDxgA5Lmu57y8Rsza0/edit).

#####   
Test Completeness

A few criteria to check Test Completeness would be

- 100% test coverage.
- All manual test cases will be executed.
- All open bugs are fixed or will be fixed in the next release.
- Fulfillment of the Acceptance Criteria.
- The feature must incorporate the client feedback while releasing the feature.
- In case of no bug, the team must have a discussion and close that ticket.

##### Test Deliverables

Test deliverables are provided as below:

**Before Testing Phase**

- Preparation of the Test Plan document.
- Preliminary preparation of the Test Case document.
- Review the Acceptance Criteria.

##### During the Testing

- Gather the Test Data
- Complete the Test Case document
- Move JIRA tickets to the done

##### After the testing cycle is over

- Test Results/Report
- Defect Report /Diagnostic Report
- Prepare a user manual for the release
- Installation guide / Deployment Instruction (if needed)
- Prepare a Release note.

##### Test Process

  
Testing must be planned and it requires discipline to act upon it. The quality and effectiveness of software testing are primarily determined by the quality of the test processes used.  
The activities of testing can be divided into the following basic steps:

- Planning and control
- Analysis and Design
- Implementation and Execution
- Evaluating exit criteria and Reporting
- Test Closure Activities

Please follow the below attached [link](https://www.toolsqa.com/software-testing/test-process-in-software-testing/) for a better understanding.

##### Roles and Responsibilities

<table border="1" id="bkmrk-s.n.-roles-responsib" style="border-collapse: collapse; width: 100%;"><tbody><tr><td style="width: 25%;">S.N.</td><td style="width: 25%;">Roles</td><td style="width: 31.4198%;">Responsibilities</td><td style="width: 18.5802%;">Remarks</td></tr><tr><td style="width: 25%;">1</td><td style="width: 25%;">Quality Assurance Engineer</td><td style="width: 31.4198%;">- Manual Testing
- Automation Testing
- Non Functional Test
- API Tests
- Preparation of all the documents and reports.

</td><td style="width: 18.5802%;"> </td></tr></tbody></table>

##### Risks, Issues, and Dependencies

The team will perform a short triage meeting where they discuss the severity of the defects/bug and prioritize accordingly. The team should work on assigning the bug to the developer without being hampered in the sprint cycle.  
Please go to the Section Defect tracking and reporting section.

##### List of Approvals

A list of the team members will approve the documents

<table border="1" id="bkmrk-s.n.-name-role-1-%C2%A0-p" style="border-collapse: collapse; width: 100%;"><tbody><tr><td style="width: 50%;">S.N.</td><td style="width: 25%;">Name</td><td style="width: 25%;">Role</td></tr><tr><td style="width: 50%;">1</td><td style="width: 25%;"> </td><td style="width: 25%;">Product Owner</td></tr><tr><td style="width: 50%;">2</td><td style="width: 25%;"> </td><td style="width: 25%;">Development Lead</td></tr></tbody></table>

##### Terms/Acronyms

  
List of the Acronyms mostly used in the project.

<table border="1" id="bkmrk-term%2Facronym-definit" style="border-collapse: collapse; width: 100%;"><tbody><tr><td style="width: 50%;">**Term/Acronym**</td><td style="width: 50%;">**Definition/Full Form**</td></tr><tr><td style="width: 50%;">UAT</td><td style="width: 50%;">User Acceptance Test/ing</td></tr><tr><td style="width: 50%;">API</td><td style="width: 50%;">Application Program Interface</td></tr><tr><td style="width: 50%;">TDD</td><td style="width: 50%;">Test-Driven Development</td></tr><tr><td style="width: 50%;">BDD</td><td style="width: 50%;">Behavior Driven Development</td></tr><tr><td style="width: 50%;">UI</td><td style="width: 50%;">User Interface</td></tr><tr><td style="width: 50%;">UX</td><td style="width: 50%;">User Experience</td></tr><tr><td style="width: 50%;">MVP</td><td style="width: 50%;">Minimum Viable Product</td></tr><tr><td style="width: 50%;">SOW</td><td style="width: 50%;">Statement of Work</td></tr><tr><td style="width: 50%;">E2E Test</td><td style="width: 50%;">End to End Test</td></tr><tr><td style="width: 50%;">B2B</td><td style="width: 50%;">Business to Business</td></tr><tr><td style="width: 50%;">B2C</td><td style="width: 50%;">Business to Customer/Consumer</td></tr></tbody></table>