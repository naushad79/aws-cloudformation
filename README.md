# AWS Cloudformation

There are AWS CloudFormation templates with examples which used for creating various AWS resources.

##cft-sample1

This cloudformation template creates a ec2 instance and a security group, security group will be attached to the ec2 instance and that allows ssh connection to the ec2 instance.

I have also used join Intrinsic Function in this example

Make sure to change the ImageId based on the region, in this example image is selected based on Sydney region.

##cft-sample2

In this cloudformation template we are using Pseudo Parameters and I have used AWS::Region, AWS::StackName and AWS::StackId.

There are others Pseudo Parameters but I have only used 3 of them

##cft-sample3

In this cloudformation template EC2 instance will get the AMI based on the mapping created within the Mappings section, using the Intrinsic Function FindInMap to find the AMI ID from the Mappings.

##cft-sample4

In this cloudformation template EC2 instance will be crated and a key is associated with the ec2 instance for SSH.

This also allows user to select the key and the instance type during the cloudformation wizard.

Note: You have to create some KeyPair before starting the cloudformation stack

You will be able to see a small list of instances in the list, if required you can add all the instances type in the list

##cft-sample5

In this cloudformation template EC2 instance will output the DNS name, public ip, private ip and the vpc id.

You will be able to see the output in the output tab in the cloudformation aws console.

Note: You need to have some KeyPair before starting the cloudformation stack
