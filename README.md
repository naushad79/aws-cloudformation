# AWS Cloudformation

There are AWS CloudFormation templates with examples which used for creating various AWS resources.

## cft-sample1

This cloudformation template creates a ec2 instance and a security group, security group will be attached to the ec2 instance and that allows ssh connection to the ec2 instance.

I have also used join Intrinsic Function in this example

Make sure to change the ImageId based on the region, in this example image is selected based on Sydney region.

## cft-sample2

In this cloudformation template we are using Pseudo Parameters and I have used AWS::Region, AWS::StackName and AWS::StackId.

There are others Pseudo Parameters but I have only used 3 of them

## cft-sample3

In this cloudformation template EC2 instance will get the AMI based on the mapping created within the Mappings section, using the Intrinsic Function FindInMap to find the AMI ID from the Mappings.

## cft-sample4

In this cloudformation template EC2 instance will be crated and a key is associated with the ec2 instance for SSH.

This also allows user to select the key and the instance type during the cloudformation wizard.

Note: You have to create some KeyPair before starting the cloudformation stack

You will be able to see a small list of instances in the list, if required you can add all the instances type in the list

## cft-sample5

In this cloudformation template EC2 instance will output the DNS name, public ip, private ip and the vpc id.

You will be able to see the output in the output tab in the cloudformation aws console.


## cft-sample6

In this cloudformation template EC2 instance will be created and update the operating system and then installs apache on the ec2 Instance

It also creates index.html file in the /var/www/html and updates the files permission

once it's done apache service will be started and also enables the service to start on boot.

once the cloudformation template is completed get the DNS name from the output tab and load it in a new tab.

I have also update the security group enable port 80 access from public


## cft-sample7

In this cloudformation template UserData and Helper Scripts are used. It update the instance, installs the AWS CFN Bootstrap and Install the files and packages from the metadata

In the AWS::CloudFormation::Init config section it installs httpd and php. It creates 2 files named /var/www/html/index.php and /var/www/html/phpinfo.php. Also it starts the httpd service and enable at boot.


once the cloudformation template is completed go to the output tab, you should be able to find the webpage url and the phpinfo page url.

Security group is updated to allow port 80 access from public.
