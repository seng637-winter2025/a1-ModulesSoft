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
| **Best Suited For**   | Identifying unknown issues, usability testing, and early-stage testing. | Ensuring compliance with functional requirements and regression testing. |
| **Skills Required**   | Requires experience, domain knowledge, and critical thinking skills. | Requires knowledge of functional requirements and test execution skills. |
| **Testing Approach**  | Unscripted, exploratory, and adaptive. | Structured, scripted, and follows a predefined test plan. |
| **Test Execution**    | Conducted in real time with minimal preparation. | Follows a structured execution based on test cases. |
| **Defect Discovery**  | Effective in identifying hidden defects and unexpected issues. | Ensures expected functionality works as intended, but may miss edge cases. |

Both exploratory and manual functional testing have their strengths and limitations. Exploratory testing is more effective in uncovering unexpected issues but requires skilled testers and lacks structured documentation. Manual functional testing ensures systematic verification of requirements but may be slower and miss unforeseen defects. A balanced approach combining both can maximize test coverage and software quality.

# Scope of Testing

The scope of testing for this ATM system includes verifying core functionalities, user interactions, and error handling.

Features to be tested:

1. **System Startup & Shutdown**: Ensures the ATM starts up correctly, accepts initial cash input, and establishes a connection with the bank. Verifies that the system shuts down properly when the power switch is turned off.

2. **Session Management**: Validates the ATM's ability to read valid ATM cards and reject unreadable ones. Ensures secure authentication by handling PIN input and verifying correctness. Supports multiple transactions within a single session and proper session termination.

3. **Transaction Processing**  
   - **Withdrawals**: Checks proper account selection, cash dispensing, balance verification, and handling of insufficient funds.  
   - **Deposits**: Verifies deposit acceptance, envelope handling, transaction logging, and cancellation scenarios.  
   - **Transfers**: Confirms accurate fund transfers between accounts, validation of transfer amounts, and transaction logging.  
   - **Inquiries**: Ensures accurate balance inquiries and transaction logs.

4. **Error Handling & Security**: Handles invalid PIN attempts with retry limits and appropriate messaging. Ensures proper cancellation of transactions at different stages. Validates system responses when cash or funds are insufficient.

Features not to be tested:
1. **Hardware Failures**: The test cases do not cover failures such as card reader malfunctions or printer issues.
2. **Network Failures**: The test plan assumes a stable connection to the bank and does not include network outage scenarios.
3. **Security Attacks**: No penetration testing or fraud detection is included in this scope.

This structured approach ensures that the ATM system operates reliably, meets functional requirements, and provides a seamless user experience.

# Test Logistics

1. **Who will test?**  
   For the test logistics, each team member was assigned specific functionalities to ensure comprehensive coverage and efficient execution. Yousef was responsible for testing core ATM operations, including system startup and shutdown, session management, and authentication processes such as card reading and PIN verification. Riley focused on transaction-related functionalities, including withdrawals, deposits, transfers, and balance inquiries, ensuring that each operation was processed correctly and logged accurately. Both team members collaborated on error handling scenarios, such as invalid PIN attempts and transaction cancellations, to validate system security and reliability. This structured division of responsibilities ensured that all functionalities were thoroughly tested while maintaining efficiency and accuracy in reporting.

3. **When will test occur?**  
   The testers will start the test execution when the following inputs are ready:  
   - Software v1.0 and v1.1 are available for testing  
   - Test Specification is created  
   - Enough human resource for testing

# Notes and discussion of the peer reviews of defect reports

During the peer review of defect reports, the team focused on ensuring clarity in defect descriptions, including clear steps to reproduce. Prioritization was discussed, emphasizing critical defects over minor ones, and reviewers considered the impact of issues on user experience. The team also addressed consistency in the reporting format to maintain clarity and ease of tracking. These discussions helped improve the quality of defect documentation and streamlined the issue resolution process.

# How the pair testing was managed and team work/effort was divided

In this pair testing approach, Yousef and Riley collaborated to ensure an efficient and well-documented testing process. Yousef was responsible for executing the test instructions on the application, interacting with the system, and identifying any issues or unexpected behaviors. Meanwhile, Riley focused on updating the report in real time, documenting test results, noting any defects, and ensuring all observations were accurately recorded. This division of work allowed for a streamlined process where both team members could focus on their respective tasks without distractions, leading to more thorough testing and precise documentation. Their teamwork ensured that any issues were captured and documented.

# Difficulties encountered, challenges overcome, and lessons learned

During the peer review of defect reports, the team noted that in some cases, the issue was not aligned with the expected outcome. For instance, when testing whether the receipt was printed correctly for a transaction, the receipt itself was fine, but the card number displayed was incorrect. These kinds of discrepancies led to deeper discussions about the actual issues and helped ensure that defect reports accurately reflected the true problem. The team also emphasized the importance of checking for unexpected issues that might not be part of the initial test case.

# Comments/feedback on the lab and lab document itself

Shorten the problem description, please.
