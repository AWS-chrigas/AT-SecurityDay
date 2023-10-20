**INSTRUCTIONS** to enable AWS Config Recorder in Multiple Regions with AWS CloudFormation Stack and StackSets.

* This set of instructions replaces the `Enable AWS Config Recorder in Multiple Regions with AWS CloudFormation StackSets` section in Workshop Studio.
* Download this .zip file, unzip the files on your laptop and follow the steps below.


## STEP 1 - Create the ServiceLinkedRole for AWS Config 

- Navigate to AWS CloudFormation console Stack.
- Click Create Stack - With new resources (standard).
- In Prerequisite - Prepare Template, select Template is ready
- In Specify template, select Upload a template file
- From the unzipped files, choose `STEP1-ServiceLinkedRole-Stack.yml` as template file to upload and click Next.
- Provide the Stack name ServiceLinkedRoleStack and click Next.
- Leave the Configure stack options section as default and click Next.
- At the bottom of Review ServiceLinkedRoleStack click Submit.


## STEP 2 - Enable AWS Config Recorder in Multiple Regions with AWS CloudFormation StackSets

- Navigate to AWS CloudFormation console StackSets.
- Click Create Stackset.
- In Permissions, under IAM role name select AWSCloudFormationStackSetAdministration role.
- In the IAM execution role name section, select AWSCloudFormationStackSetExecution role.
- In Prerequisite - Prepare Template, select the option Template is ready.
- In Specify template, select Upload a template file
- From the unzipped files, choose `STEP2-AWSConfigRecorder-StackSet.yml` as template file to upload and click Next.
- Provide the StackSet name AWSConfigStackSet, leave the parameters as default and click Next.
- Leave the Configure StackSet options section as default and click Next.
- In the Account sections, select Deploy stacks in accounts.
- Under Account Numbers provide your current AWS Account Id (you click-to-copy it in the top right corner of the console).
- Under Specify regions choose US East (N.Virginia) and US West (Oregon) .
- Leave the Deployment options as default and click Next.
- Review the options and click Submit. It will take approximately 2 minutes.