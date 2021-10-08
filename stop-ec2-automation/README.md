Stop an EC2 Instance with Lambda in AWS

1. Create the Lambda function, using stopEC2instances.py python code.

2. Apply execution policy to the Lambda function. 

3. Set the lambda function timeout more than 1 min due to it need to scan through all region.

4. Run a test for the Lambda function.

5. If you need to setup the cron job to stop the instance please use AWS EventBridge


![Screen Shot 2021-10-08 at 8 53 38 am](https://user-images.githubusercontent.com/66815986/136484040-2d32f6e6-3df2-425b-9b07-dd0666039b66.png)
