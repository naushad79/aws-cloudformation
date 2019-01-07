# Use of UserData in CloudFormation

In this cloudformation template EC2 instance will be created and update the operating system and then installs apache on the ec2 Instance

It also creates index.html file in the /var/www/html and updates the files permission

once it's done apache service will be started and also enables the service to start on boot.

once the cloudformation template is completed get the DNS name from the output tab and load it in a new tab.

I have also update the security group enable port 80 access from public

Note:
You need to have some KeyPair before starting the cloudformation stack
