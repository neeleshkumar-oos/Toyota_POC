1. **INTRODUCTION**
1.1.	Overview
The purpose of this Test Plan Specification is to describe the scope, approach, resources, and schedule of testing activities supported by Testing team. The Test Plan serves as the controlling standards document for defining and developing test scenarios and conducting the testing.  The end result of completing this plan is to provide a guideline or testing roadmap for employees to achieve validation and verification.

1.2 **Objectives**
The objective of this POC Test Plan is to define the procedures and logistics necessary     @@@@to
test the functionality of equipment and applications associated with Toyota-POC.
This functionality has been defined in previous documents as use cases and requirements.
The following objectives were incorporated into the test plan:
• Provide a formal testing process
• Test each Sprintwise requirement 
• Document the results of each test
• Collect data from the tests
• Provide useable information from which to develop the final documents such as—
– Final design
– Benefit-cost analysis
– Transition plan
• Provide verifiable documentation that the concept, as developed, is functional.

1.3.	**Scope**
This Proof-of-concept (PoC) is to demonstrate Connected Car Cloud framework highlighting real-time 2-way communication from Edge to Cloud and access to Cloud framework for Customer’s R&D Engineers. This framework will demonstrate data ingestion to cloud for further data classification, storage and processing. The vehicle data includes CAN data as well as other complementary sensing data such as JSON and binary data. In order to demonstrate the 2-way communication, this PoC will implement functionalities to support real-time downstream messaging from the Cloud to the Edge.

**Product Scope**:
The secured MQTT endpoints hosted on AWS IoT Core with certificate based authentication will be created. These MQTT endpoints will support publish/subscribe communication using JSON or Binary encoded payload with maximum payload size of 128KB limited by AWS IoT capabilities. Additionally, secured HTTP endpoints will also be developed for supporting larger sized payloads with maximum per request size of 10MB as limited by AWS API Gateway. Any larger sized payload of more than 10MB will have to split into multi-part request from client side, for example, Edge Applications. These MQTT and HTTP endpoints will be used to upload vehicle CAN data predecoded by Edge application and transmitted as either JSON or binary payload. HTTP endpoints will be used to manage map navigation data in the PoC. Map Navigation data will be static and preferably stored in AWS S3 bucket.

2. **General Testing Methodology**
This POC test plan is designed to test the high level (Tier 1) requirements as developed
and documented in the Requirements document. These requirements
are not a complete list of all functions rather they are a basic set of requirements
Each test associated with a requirement is described,
along with the test procedure. The basic format of each requirement is
• Test Description—Provides a brief overview of the test
• Test Procedures—Lists the test steps
• Expected Results—Describes what is expected to happen
• Pass/Fail—Will be used during the actual test to record Pass or Fail
• Results—Will be used during the actual test to document the results of the test. 

3. **Sprint Phases**
3.1. Company Sprint is divided into 4 phases, typically 2 weeks each, 
a) Grooming 
b) Pre Sprint 
c) Dev Integration 
d) Post Sprint


4.	**TEST STRATEGY**
1.	Scope of Testing and tools for testing

a)	Backend Testing  @tools--PostMan and  MQTT-Spy
b)	Database Testing--Performed by Manual tesing,We are doing R&D for AUtomation testing once get idea we will move into Automation.
c)	UI Testing---Jest tool
d)	Performance Testing--JMeter

2.	Testing is performed on Test environment and Production environment.

3.	The priority of testing activity
a)	Smoke test of every build
b)	Defects Validation
c)	New features testing
d)	Regression testing

4.1	**Type of testing**
I.	**System Testing**
System Testing is performed on Test Environment to thoroughly test all the New Features and Regression, in order to uncover defects and issues. The testing of software components, hardware components, or both, are combined and tested to evaluate the interaction between them. The main intent is to test all the code changes against requirements for the release
II.	**Integration Testing**
Integration Testing is performed to uncover defects in the interfaces and in the interactions between integrated components or systems. It is performed mainly to testing the software at interface levels as a group.
III.	**Production Testing**
The Production Testing is performed on the Production environment, once the testing is complete on Test Environment.

4.2	**Validation**
All the defects opened by the testing team will be validated and closed.
4.3	**Testing Tools**
1.	Eclipse
2.	 Selenium server
3.	GitHub
4.	Operating system: Win 10
5.	Browser – Google Chrome, IE, Firefox, Safari,Edge
6.	JMeter
7.	Defect Life management tool(Kindly suggest)

5.	**TEST PREPARATION:  PROCEDURES AND DOCUMENTATION**
5.1.	Test Case Preparation

5.2.	Test Environment Set Up

5.3.	Database Set Up

6.	**Test Data Strategy & Test Automation Script Development** 
1.	The testing of use cases implemented is mainly carried out with the data provided by Customer.
2.	The Automation QA team uses the functional / regression test cases to develop Automation Test Descriptions in preparation for automation with the help of Services/UI as part of Data Driven Development. Automation Testers complete the Automation Scripts and start executing them against each build. The automation scripts will go through continuous maintenance as the product evolves and bugs are fixed. 
3.	Performance QA performs tests against the services and UI.
