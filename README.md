# delete_unused_ami
Deregistering/deletion of AMI which are older than 3 months and are not in use in order to optimize cost.

Delete Unused AMI's - Using Python

The AMI's created in your AWS account has a huge impact on your monthly bill. This happens when we create a lot of AMI either manually or by script for backup purpose. So in order to optimise cost we must delete the unused AMI's since they are increasing cost even if they are used or not. These AMI are used by snapshots which can not be deleted before de-registering the AMI.

Problem Statement: 
Deregistering/deletion of AMI which are older than 3 months and are not in use in order to optimize cost.
