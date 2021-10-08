Delete unattached EBS volume with Lambda in AWS

1. Before using lambda to delete unattached ebs volume, unttached EBS volume require to change termination policy to false. 
- cat mapping.json #to check the ebs volume device name

- aws ec2 modify-instance-attribute --instance-id INSTANCE-ID --block-device-mappings file://mapping.json