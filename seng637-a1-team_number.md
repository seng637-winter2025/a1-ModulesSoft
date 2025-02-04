> **SENG 637 - Software Testing, Reliability, and Quality**

**Lab. Report #1 – Introduction to Testing and Defect Tracking**

| Group: 23      |
|-----------------|
| Riley Koppang                |   
| Yousef Fatouraee              |   

**Table of Contents**

1. [Introduction](#introduction)  
2. [High-level description of the exploratory testing plan](#high-level-description-of-the-exploratory-testing-plan)  
3. [Comparison of exploratory and manual functional testing](#comparison-of-exploratory-and-manual-functional-testing)  
4. [Notes and discussion of the peer reviews of defect reports](#notes-and-discussion-of-the-peer-reviews-of-defect-reports)  
5. [How the pair testing was managed and team work/effort was divided](#how-the-pair-testing-was-managed-and-team-workeffort-was-divided)  
6. [Difficulties encountered, challenges overcome, and lessons learned](#difficulties-encountered-challenges-overcome-and-lessons-learned)  
7. [Comments/feedback on the lab and lab document itself](#commentsfeedback-on-the-lab-and-lab-document-itself)

# Introduction

This test plan outlines the scope, approach, resources, and schedule for all testing activities related to the Gordon College ATM system simulation project. It specifies the components and features to be tested, the types of testing to be conducted, the personnel responsible, the necessary resources and timeline, and the potential risks associated with the testing process.

# Test Types

For this project, we carried out 3 types of tests:
1. Exploratory (Manual Non-scripted) Testing
2. Manual Scripted Testing
3. Regression Testing (Verification of Defect Fixes)

# High-level description of the exploratory testing plan

The exploratory testing plan focuses on dynamically investigating the Gordon College ATM system simulation without predefined test cases. Testers interacted with the system in an unscripted manner, exploring its features, workflows, and edge cases to identify unexpected behaviors, usability issues, and potential defects. This approach allows for real-time learning, test adaptation, and rapid feedback. Key areas of focus include transaction processing, user authentication, error handling, and system security. Testers documented their observations, findings, and areas requiring further investigation, ensuring comprehensive coverage of critical functionalities.

# Comparison of exploratory and manual functional testing

| Perspective            | Exploratory Testing                                    | Manual Functional Testing                              |
|------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **Definition**         | Dynamic testing approach where testers explore the application without written test cases. | Structured testing approach, testers execute predefined test cases. |
| **Benefits**          | Finds unexpected defects, provides real-time feedback when testing. | Ensures functionalities align with requirements. |
| **Tradeoffs**         | Lack of predefined structure may result in incomprehensive coverage. It also relies heavily on tester expertise. | May miss 
 some issues not included in the predefined test cases. |
| **Effectiveness**     | Good for finding unknown defects, user experience issues. | Effective in verifying expected functionality works as specified, but may overlook unexpected issues. |
| **Efficiency**        | It relies heavily on the tester's experience. | May be slower due to predefined test execution steps. |
| **Test Case Design**  | Testers create and adapt tests on the fly. | Predefined test cases based on requirements and specifications. |
| **Flexibility**       | Highly flexible | Less flexible |
| **Documentation**     | Test documentation is created based on observations. | Test cases, results, and expectations report are documented in advance. |


Both exploratory and manual functional testing have their strengths and limitations. Exploratory testing is more effective in uncovering unexpected issues but requires skilled testers and lacks structured documentation. Manual functional testing ensures systematic verification of requirements but may be slower and miss unforeseen defects. A balanced approach combining both can maximize test coverage and software quality.

# Scope of Testing

The scope of testing for this ATM system includes verifying authentication, transaction functionalities, receipt generation, logging, user interactions, and error handling.

Features to be tested:

1. **System Startup & Shutdown**: Ensuring the ATM starts up correctly, accepts initial cash bills input by the operator, and establishes a connection with the bank (server). Verifying that the system shuts down properly when the power switch is turned off and the machine is not being used.

2. **Session Management**: Validating the ATM's ability to read valid ATM cards and reject unreadable ones. Ensuring secure authentication by handling PIN input and verifying correctness. Supporting multiple transactions within a single session and the ability to cancel transaction at anytime and going back to the main menu.

3. **Transaction Processing**:  
   - **Withdrawals**: Checking proper account selection, cash dispensing, balance verification, and handling of insufficient funds.  
   - **Deposits**: Verifying deposit acceptance, envelope handling, transaction logging, and cancellation scenarios.  
   - **Transfers**: Confirming accurate fund transfers between accounts, validation of transfer amounts, and transaction logging.  

4. **Error Handling & Security**: Handling invalid PIN attempts with retry limits and appropriate messaging. Ensuring proper cancellation of transactions at different stages. Validating system responses when cash or funds are insufficient.

Features not to be tested:
1. **Hardware Failures**: The test cases do not cover failures such as card reader malfunctions, bill deposits verification, or printer issues.
2. **Security**: No penetration testing or fraud detection is included in this scope.
3. **Storing Data**: Long term data storage on the disk is not covered.
4. **Transfer Between 2 users**: Transactions between two different users are not covered.

This structured approach ensures that the ATM system operates reliably, meets functional requirements, and provides a seamless user experience.

# Test Logistics

1. **Who will test?**

   In a real-world software project, testing involves unit tests, security assessments, and structured QA processes. However, since our assignment did not include unit testing or security measures, we approached testing as a group of two using exploratory and manual testing. We actively interacted with the software, testing different inputs, edge cases, and possible failure points without writing test codes.

4. **When will test occur?**  
   The testers will start the test execution when the following inputs are ready:  
   - Software v1.0 and v1.1 are available for testing  
   - Test cases are documented  
   - Enough human resource for testing

# Notes and discussion of the peer reviews of defect reports

During the peer review of defect reports, the team focused on ensuring clarity in defect descriptions, including clear steps to reproduce. Prioritization was discussed, emphasizing critical defects over minor ones, and reviewers considered the impact of issues on user experience. The team also addressed consistency in the reporting format to maintain clarity and ease of tracking. These discussions helped improve the quality of defect documentation and streamlined the issue resolution process.

# How the pair testing was managed and team work/effort was divided

In this pair-testing approach, Yousef and Riley collaborated to ensure an efficient and well-documented testing process. For the first section, Yousef was responsible for executing the test instructions for the application and creating the exploratory test plan. Riley also contributed to the exploratory test pan and documented the results, noting any found defects. For the second part of the assignment, Riley and Yousef swapped back and forth testing the application and also giving insights about what to test.

# Difficulties encountered, challenges overcome, and lessons learned

 One of the difficulties we encountered was understanding the exact system requirements. An example of this was the internal logs of the ATM being connected to the bank. We were not sure what this log was supposed to look like and assumed it was not working. Another challenge was knowing if we should mark a bug defect for a test case that did not involve a bug. An example of this was when we tested if the receipt was being printed correctly with the correct transaction information. While everything appeared to be okay the only issue was the card number. Since there was another test in which we reported the card number was a bug, we did not know whether or not to mark this one as also a bug.

One challenge we had to overcome was understanding Jira. It seemed confusing and mundane to report bugs using this software. We had issues with the template and even when changing it, we could not create all the required column names. To overcome this we eventually transferred everything to an Excel sheet ourselves. Another challenge was understanding the system requirements as stated above. To overcome this we had to assume what the requirements were asking of us, which in a real-world situation we would ask further questions about the requirements. 

We learned to collaborate effectively and also make proper bug reports from the beginning. All the discrepancies we faced led to further discussions about the actual issues and helped us ensure that defect reports accurately reflected the true problem.

# Comments/feedback on the lab and lab document itself

Please shorten the problem description with more clarity.

It would be more practical if assignments could include practical testing with unit tests, security checks, and automation for hands-on experience, though we recognize time constraints.
