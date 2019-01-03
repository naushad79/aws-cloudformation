# Use of Mappings in CloudFormation

In this cloudformation template EC2 instance will get the AMI based on the mapping created within the Mappings section, using the Intrinsic Function FindInMap to find the AMI ID from the Mappings.

Also In this example I have not added all the regions

You can find all the regions using the following URL
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Concepts.RegionsAndAvailabilityZones.html
