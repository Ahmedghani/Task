Project Name
This project contains the backend system for generating and validating single-use tokens using AWS services.

Prerequisites
AWS CLI installed and configured with the necessary permissions.
Bash shell (e.g., Git Bash, WSL) for running the script on Windows.
AWS CloudFormation.
Steps to Set Up the Project
Clone the Repository

Clone this repository to your local machine:

bash
Copy code
git clone https://github.com/yourusername/yourrepository.git
Navigate to the project directory:

bash
Copy code
cd yourrepository
Run the Upload Script

Run the provided bash script to create the S3 bucket and upload the necessary files:

bash
Copy code
./uploadfiles.sh
Deploy the CloudFormation Stack

Go to the AWS Management Console and navigate to the CloudFormation service.

Click on Create Stack and choose With new resources (standard).
Select Upload a template file, choose the cloudformation.yml file from this repository, and click Next.
Follow the prompts and click Next until you reach the end, then click Create stack.
Get API URLs from CloudFormation Outputs

After the stack creation is complete, go to the Outputs section of the CloudFormation stack.

Copy the provided URLs for the GenerateTokenAPI and ValidateTokenAPI.
Test the APIs using Postman

Open Postman and create a new POST request.
For the Generate Token endpoint, use the copied URL for the GenerateTokenAPI and add the path /t1/generatetoken.
For the Validate Token endpoint, use the copied URL for the ValidateTokenAPI and add the path /t2/validatetoken.
Send requests to these endpoints to test the token generation and validation functionality.
