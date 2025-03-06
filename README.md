# A summary of the Artemis Financial software requirements.

**Project Notes**
Artemis Financial was requesting a check on vulnerabilities in their web app. Artemis is a Financial group that needs its web application checked to ensure the application is safe and does not have any risk of leaking vital information. Since the company deals with financial. They wanted to make sure the security of the application was there. They wanted to have extra measures added to improve the security behind the web app. The application was changed to a 256bit key to add the measure and a certified key was included for extra secure measures. The certified key was a bit challenging. With enough trial and error, the certificate key was included. I wouldn't do anything different. Testing with various applications such as Maven was done to make sure the the software was functional and secure. An extra step was done using the Maven. 

CS 305 Project One 
Artemis Financial Vulnerability Assessment Report
 
Table of Contents

Document Revision History	3
Client	3
Instructions	3
Developer	4
1. Interpreting Client Needs	4
2. Areas of Security	4
3. Manual Review	4
4. Static Testing	4
5. Mitigation Plan	4




 
Document Revision History

Version	Date	Author	Comments
1.0	1/29/2021	Kyle Ogle	

Client

 

Instructions

Deliver this completed vulnerability assessment report, identifying your findings of security vulnerabilities and articulating recommendations for next steps to remedy the issues you have found. 
Respond to the five steps outlined below and include your findings. Replace the bracketed text on all pages with your own words. If you choose to include images or supporting materials, be sure to insert them throughout.

 
Developer
Ricardo Reyes


1. Interpreting Client Needs
Determine your client’s needs and potential threats and attacks associated with their application and software security requirements. Consider the following regarding how companies protect against external threats based on the scenario information:

•	What is the value of secure communications to the company?
•	Are there any international transactions that the company produces?
•	Are there governmental restrictions about secure communications to consider?
•	What external threats might be present now and in the immediate future?
•	What are the “modernization” requirements that must be considered, such as the role of open source libraries and evolving web application technologies?

Artemis Financial provides financial plans for their customers. Since this financial information is highly sensitive, all communications between the company and their clients must be secure. Artemis Financial will also need to follow government regulations regarding financial transactions and communications, which will affect data retention policies and security requirements. In general, RESTful APIs such as Artemis Financial’s are vulnerable to data interception if requests and responses are not structured securely. In particular, the service must be sure to use HTTPS for all communications and send confidential information in request and response headers or in the request or response body. Additionally, a secure authentication scheme such as OAuth should be used.

2. Areas of Security
Referring to the Vulnerability Assessment Process Flow Diagram, identify which areas of security are applicable to Artemis Financial’s software application. Justify your reasoning for why each area is relevant to the software application.  

•	Input validation – because the RESTful API will accept user input, this input will have to be validated. The moment the user has input the validation begins. This is necessary to prevent any security risks.
•	APIs – the web service includes a RESTful API which will need to communicate securely. The API is necessary to define the user. This will run not just as internal but externally as well.
•	Code error – errors due to improper user input must be handled securely.  Errors should be handled immediately when validating to prevent any unathoried users and security risks.

3. Manual Review
Continue working through the Vulnerability Assessment Process Flow Diagram. Identify all vulnerabilities in the code base by manually inspecting the code. 

•	Business names are sent as request parameters in the CRUDController class
•	Database connection parameters are hard-coded in DocData
•	Request parameters are not validated
•	Service does not use HTTPS
•	No authentication scheme present

4. Static Testing
Run a dependency check on Artemis Financial’s software application to identify all security vulnerabilities in the code. Record the output from dependency check report. Include the following:

a.	The names or vulnerability codes of the known vulnerabilities
b.	A brief description and recommended solutions provided by the dependency check report
c.	Attribution (if any) that documents how this vulnerability has been identified or documented previously

 

5. Mitigation Plan
After interpreting your results from the manual review and static testing, identify the steps to remedy the identified security vulnerabilities for Artemis Financial’s software application.

•	Switch to HTTPS protocol for all communications
•	Move request parameters to headers or body rather than URI
•	Remove hard-coded database connection credentials
•	Implement secure authentication scheme
•	Update dependencies as listed above


