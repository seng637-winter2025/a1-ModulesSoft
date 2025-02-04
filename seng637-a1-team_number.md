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
| **Definition**         | A dynamic testing approach where testers explore the application without predefined test cases. | A structured testing approach where testers execute predefined test cases to verify functionality. |
| **Benefits**          | Uncovers unexpected defects, provides real-time feedback, and enhances creativity in testing. | Ensures system functionality aligns with requirements, provides repeatability, and facilitates regression testing. |
| **Tradeoffs**         | Lack of predefined structure may result in inconsistent coverage; relies heavily on tester expertise. | Can be time-consuming and may miss issues outside the predefined test cases. |
| **Effectiveness**     | Highly effective for finding unknown defects, usability issues, and edge cases. | Effective in verifying that expected functionality works as specified, but may overlook unexpected issues. |
| **Efficiency**        | Faster in identifying critical issues but may require repeated testing due to lack of documentation. | Systematic and structured, but may be slower due to predefined test execution steps. |
| **Test Case Design**  | No predefined test cases; testers create and adapt tests on the fly. | Predefined test cases based on requirements and specifications. |
| **Flexibility**       | Highly flexible, allowing testers to investigate issues as they arise. | Less flexible, as tests follow a structured plan. |
| **Documentation**     | Test documentation is created dynamically based on observations. | Test cases, results, and defect reports are documented in advance. |


Both exploratory and manual functional testing have their strengths and limitations. Exploratory testing is more effective in uncovering unexpected issues but requires skilled testers and lacks structured documentation. Manual functional testing ensures systematic verification of requirements but may be slower and miss unforeseen defects. A balanced approach combining both can maximize test coverage and software quality.

# Scope of Testing

The scope of testing for this ATM system includes verifying authentication, transaction functionalities, receipt generation, logging, user interactions, and error handling.

Features to be tested:

1. **System Startup & Shutdown**: Ensuring the ATM starts up correctly, accepts initial cash bills input by the operator, and establishes a connection with the bank (server). Verifying that the system shuts down properly when the power switch is turned off and the machine is not being used.

2. **Session Management**: Validating the ATM's ability to read valid ATM cards and reject unreadable ones. Ensuring secure authentication by handling PIN input and verifying correctness. Supporting multiple transactions within a single session and the ability to cancel transaction at anytime and going back to the main menu.

3. **Transaction Processing**  
   - **Withdrawals**: Checking proper account selection, cash dispensing, balance verification, and handling of insufficient funds.  
   - **Deposits**: Verifying deposit acceptance, envelope handling, transaction logging, and cancellation scenarios.  
   - **Transfers**: Confirming accurate fund transfers between accounts, validation of transfer amounts, and transaction logging.  

4. **Error Handling & Security**: Handles invalid PIN attempts with retry limits and appropriate messaging. Ensures proper cancellation of transactions at different stages. Validates system responses when cash or funds are insufficient.

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

In this pair testing approach, Yousef and Riley collaborated to ensure an efficient and well-documented testing process. Yousef was responsible for executing the test instructions on the application, interacting with the system, and identifying any issues or unexpected behaviors. Meanwhile, Riley focused on updating the report in real time, documenting test results, noting any defects, and ensuring all observations were accurately recorded.

# Difficulties encountered, challenges overcome, and lessons learned

During the peer review of defect reports, the team noted that in some cases, the issue was not aligned with the expected outcome. For instance, when testing whether the receipt was printed correctly for a transaction, the receipt itself was fine, but the card number displayed was incorrect. These kinds of discrepancies led to deeper discussions about the actual issues and helped ensure that defect reports accurately reflected the true problem. The team also emphasized the importance of checking for unexpected issues that might not be part of the initial test case.

# Comments/feedback on the lab and lab document itself

please shorten the problem description with more clarity.
It would be more practical if assignments could include practical testing with unit tests, security checks, and automation for hands-on experience, though we recognize time constraints.
