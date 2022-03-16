Create an EC2 Snapshot with Lambda in AWS

1. Create the Lambda function, using ec2-backup.py python code.

2. Apply execution policy to the Lambda function. 

3. Set the lambda function timeout more than 1 min due to it need to scan through all region.

4. Run a test for the Lambda function.

5. If you need to setup the cron job to stop the instance please use AWS EventBridge.

6. Same procedue for deleting snapshot.
