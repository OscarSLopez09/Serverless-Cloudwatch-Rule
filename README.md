# Let's start with a high level overview.
A rule can run in response to an event or at certain time intervals. For example, to periodically run an AWS Lambda function, you can create a rule to run on a schedule.
Using Cloudwatch events, I will configure a rule to trigger a lambda function every three minutes.

Let's start by going to the AWS console and typing CloudWatch. On the left pane of the CloudWatch dashboard, go to events and click on rules.

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* On the rules page, select Create Rule.

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch0.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Now, the define details rules page opens and we define the rule name - NewsSentimentReader

* On the rule type select - Schedule 

* Click on - Continue to create rule 

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch01.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* On schedule patterns select - A schedule that runs at regular rate, such as every 10 minutes.
* Set the rule to run every 3 minutes and selct next

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch02.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Target type - select AWS Service 
* Select a target type - Lambda function
* On Function, select the Lambda function - NewsReaderAPI
* Click on next
<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch03.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Click on additional settings
* Configuration target input - Constant (JASON text)
* Specify the constant in JSON - {"action":"insert news"}

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch04.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Scroll down and click on next

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch05.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* On Review and create scrolld down and click on create

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch06.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Now we wait for a couple of minutes for the rules to start triggering the lambda function
* Go back to AWS lambda console and click on NewsReaderAPI

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch07.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Go to monitoring and View cloudwatch logs

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch08.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Select a log stream and check that the rule is being trigger every 3 minutes

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch09.PNG" height="80%" width="80%" alt="Disk Sanitization Steps"/>

* Rule being trigger every 3 minutes

<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch010.PNG" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/OscarSLopez09/Serverless-Cloudwatch-Rule/blob/main/Images/cloudwatch011.PNG" height="100%" width="100%" alt="Disk Sanitization Steps"/>





