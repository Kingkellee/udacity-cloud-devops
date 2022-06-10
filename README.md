### Project Title - Deploy a high-availability web app using CloudFormation

This folder provides the Solutions to the Udacity NanoDegree Project 2 Submitted by Kelly Iyogun

The Project Submission Files Include

# 1. udagram-net-infra.yml

This contains the VPC, NATGateways, Route, Routing Table,Public and Private Subnets.

# 2. udagram-net-infra-params.json

Parameters value for our Infrastructure

# 3. udagram-server-infra.yml

This contains our Loan Balancer, Security Group, LaunchConfiguration, AutoScaling Group and Target Group

# 3. udagram-server-params.json

Parameters need to deploy our Network Infrastructure

# 4. Cloud Infrastructure Diagram

Udagram-Cloud-Diagram.png

# 5. Image Result

You can see a screenshot of all resources, outputs and a deployed running website here

#### Prerequisite?

You should have

1. A user with Programatic Access to AWS
2. Install AWSCLI https://aws.amazon.com/cli/

### To Use

Begin by Cloning, downloading this project

Then run;
aws cloudformation create-stack --stack-name Your-Stack-Name-Here --template-body file://udagram-net-infra.yml --parameters file://udagram-net-params.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=your-aws-region

do the same with the server YAML and JSON file....

Better, you could run the bash script

./create.sh Your-Stack-Name-Here template.yml template-params.json
./update.sh Your-Stack-Name-Here template.yml template-params.json

to delete, you can simply run:
aws clouformation delete-stack Your-Stack-Name-Here

or run
./destroy.sh Your-Stack-Name-Here

### Output

Load Balancer DNS: http://udagr-udagr-1m1lw1617zwo7-1534993903.us-east-1.elb.amazonaws.com/
