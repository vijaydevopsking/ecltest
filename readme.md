**Step-by-Step Guide for AWS CloudFormation Template**
**Overview**
This guide provides detailed steps for using the provided AWS CloudFormation template to set up an AWS Elastic Beanstalk environment without SSL. This template automates the creation of the necessary AWS resources, including VPC, subnets, internet gateway, and Elastic Beanstalk configurations.

Prerequisites
1. An AWS account with necessary permissions to create the resources outlined in the template.
2. AWS CLI installed and configured on your local machine, or access to the AWS Management Console.
3. Type below command in your local to check the existing solutions available for elastik bean stack i have picked PHP you can pick as your reuirements this is manadatory step.
    aws elasticbeanstalk list-available-solution-stacks
4. Once you get the list please update in the template with your solution below line.
SolutionStackName: 64bit Amazon Linux 2 v3.5.14 running PHP 8.1 (your solution name)
 
   
Steps
1. Prepare the CloudFormation Template
Download the provided CloudFormation template to your local system.
2. Upload the Template to AWS
Log in to the AWS Management Console.
Navigate to the CloudFormation service.
Click on "Create stack" and select "With new resources (standard)".
Choose "Upload a template file", click "Choose file", and select the downloaded template.
Click "Next" to proceed.
3. Configure Stack Details
Enter a stack name. This name will be used to identify this particular stack within AWS CloudFormation.
Since there are no parameters to configure in this template, click "Next" to proceed.
4. Configure Stack Options
Optionally, you can configure tags, permissions, and other advanced options. However, for most scenarios, you can leave these as default.
Click "Next" to proceed.
5. Review and Create the Stack
Review the configurations to ensure everything is correct.
Acknowledge that AWS CloudFormation might create IAM resources by checking the box at the bottom.
Click "Create stack" to start the creation of the resources as defined in the template.
6. Monitor the Stack Creation
The AWS Management Console will display the stack status. Wait until the status changes to "CREATE_COMPLETE". This might take several minutes.
In case of errors, AWS CloudFormation will roll back changes. Check the "Events" tab for logs to troubleshoot.
7. Access the Elastic Beanstalk Environment
Once the stack creation is complete, navigate to the Elastic Beanstalk service in the AWS Management Console.
You should see the newly created application and environment. You can now deploy your application to this environment.
8. Cleanup
To delete the resources, return to the CloudFormation console.
Select the stack you created, click "Delete", and confirm. AWS CloudFormation will then remove all resources associated with the stack
