Delete unattached EBS volume with Lambda in AWS

1. Before using lambda to delete unattached ebs volume, unttached EBS volume require to change termination policy to false. 
- cat mapping.json #to check the ebs volume device name

- aws ec2 modify-instance-attribute --instance-id INSTANCE-ID --block-device-mappings file://mapping.json

2. Create the Lambda function, using delete-ebs.py python code.

2. Apply execution policy to the Lambda function. 

3. Set the lambda function timeout more than 1 min due to it need to scan through all region.

4. Run a test for the Lambda function.

5. If you need to setup the cron job to stop the instance please use AWS EventBridge.
