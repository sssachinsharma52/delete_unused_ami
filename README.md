# delete_unused_ami

**Problem Statement:**
Deregistering/deletion of AMI which are older than 3 months and are not in use in order to optimize cost.

**Delete Unused AMI's - Using Python**

The AMI's created in your AWS account has a huge impact on your monthly bill. This happens when we create a lot of AMI either manually or by script for backup purpose. So in order to optimise cost we must delete the unused AMI's since they are increasing cost even if they are used or not. These AMI are used by snapshots which can not be deleted before de-registering the AMI.


**AMI:** An Amazon Machine Image (AMI) provides with the required information to launch an EC2 instance containing one or more snapshots, launch permissions and block device mapping.

**Brief of the overall process is explained below:**

- Get all the AMI created in your account:
- Find AMI which are not in used from EC2 instances.
- Deregister the AMI’s.



**Logic and functions of script**

- ami_from_ami_list(): Run ec2 describe-images from aws cli to get the list of all AMI in your account which are older than 3 months (say List 1).
- ami_from_ec2_instances(): Run ec2 describe-instances from aws cli to get list of attached AMI’s or AMI in use (say List 2).
- ami_not_in_use(): Find AMI’s which are not in use i.e. AMI’s in list 1 but not in list 2.
- deregister_ami(): Run AWSderegister function to deregister the AMI’s.

**Requirements**

- AWS Account number: Your AWS account number.
- AWS (aws-cli) profile name: Your aws-cli profile name.
 

