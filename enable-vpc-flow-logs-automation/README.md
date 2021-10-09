Enable VPC flow log whenever new VPC created

1. Create cloudwatch event pattern rule using event-pattern.json

2. Create lambda function using enable-vpc.py 

3. Apply execution policy to the Lambda function. 

4. Set the lambda function timeout more than 1 min due to it need to scan through all region.

5. Create environment variable in lambda function FLOWLOGS_GROUP_NAME & ROLE_ARN for vpc flow log logging

Example

FLOWLOGS_GROUP_NAME cfst-746-03bb6eb9e4f5932970dd0f8f19142438-VPCFlowLogsLogGroup-JNbJoTssVzwX
ROLE_ARN arn:aws:iam::222601037781:role/cfst-746-03bb6eb9e4f5932970-DeliverVPCFlowLogsRole-NL6BC0CPFW3P

6. Run a test for the Lambda function.

