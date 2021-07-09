# nd9991-03-IaC
This is the final project `Deploy a high-availability web app using CloudFormation` from the third part of the course [Cloud DevOps Engineer](https://www.udacity.com/course/cloud-dev-ops-nanodegree--nd9991).

Assigned task: deploy an high-availability web application from an S3 bucket into AWS in an automated way.

## How to create the CloudFormation stack

    $ cat create.sh
    aws cloudformation create-stack --stack-name $1 --template-body file://$2  --parameters file://$3 --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-
    
    $ ./create.sh project02 project02.yml project02-parameters.json
