# Use of Helper Script in CloudFormation

In this cloudformation template UserData and Helper Scripts are used. It update the instance, installs the AWS CFN Bootstrap and Install the files and packages from the metadata

In the AWS::CloudFormation::Init config section it installs httpd and php. It creates 2 files named /var/www/html/index.php and /var/www/html/phpinfo.php. Also it starts the httpd service and enable at boot.


once the cloudformation template is completed go to the output tab, you should be able to find the webpage url and the phpinfo page url.

Security group is updated to allow port 80 access from public.

Note:
You need to have some KeyPair before starting the cloudformation stack
