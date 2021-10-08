Deregistering an old ami with Lambda in AWS

1. Create the Lambda function, using deregister-ami.py python code.

2. Apply execution policy to the Lambda function. 

3. Set the lambda function timeout more than 1 min due to it need to scan through all region.

4. Run a test for the Lambda function.

5. If you need to setup the cron job to stop the instance please use AWS EventBridge.

Example Output:
![image](https://user-images.githubusercontent.com/66815986/136634949-e2577b5b-7b9c-4daa-8684-e21f0a7752d6.png)

