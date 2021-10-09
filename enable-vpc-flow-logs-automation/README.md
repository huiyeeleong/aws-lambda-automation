Enable VPC flow log whenever new VPC created

1. Create cloudwatch event pattern rule using event-pattern.json

2. Create lambda function using enable-vpc.py 

3. Apply execution policy to the Lambda function. 

4. Set the lambda function timeout more than 1 min due to it need to scan through all region.

5. Run a test for the Lambda function.

