# aws-lambda-automation-python
This is a collection of AWS lambda function that perform automation using python and boto3

Prerequisite for boto3

A low-level interface to a growing number of Amazon Web Services. The botocore package is the foundation for the AWS CLI as well as boto3.

On 01/15/2021 deprecation for Python 2.7 was announced and support was dropped on 07/15/2021. To avoid disruption, customers using Botocore on Python 2.7 may need to upgrade their version of Python or pin the version of Botocore. For more information, see this blog post.

Launch an linux ec2 instance or using your local machine
1. SSH into instance if its launch from ec2. If you are using local machine please proceed to number 3.

2. Update new packages on ec2 linux 
- sudo yum update

3. Install python3 
- sudo yum install -y python3-pip  python3-pip python3-setuptools

4. Install boto3 
- pip3 install boto3 --user

5. Check python version 
- python3 --version

Using Botocore
After installing botocore

Set up aws credentials (credentials will located in ~/.aws/credentials):

Documentation on how to setup aws credentials: https://docs.aws.amazon.com/sdk-for-java/v1/developer-guide/setup-credentials.html

- aws configure --profile YOUR-PROFILE-NAME

aws_access_key_id = YOUR_KEY
aws_secret_access_key = YOUR_SECRET
region = AWS_REGION
output = json

Check if AWS credentials configure appropriately
- aws sts get-caller-indetity

e.g To check s3 bucket using Python Boto3 interpreter:
>>> import boto3
>>> s3 = bot3.resource
>>> for bucket in s3.buckets.all():
>>> print(bucket.name)

e.g Launch ec2 instance using Python Boto3 interpreter:
This will launch a brand new instance
>>> import boto3
>>> response = ec2.run_instances(
>>>     ImageId = 'ami-02e136e904f3da870',
>>>     InstanceType = 't2.micro'
>>>     KeyName= 'demo-ap-southeast-2'
>>>     MinCount = 1,
>>>     MaxCount = 1
>>> )