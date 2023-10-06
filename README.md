# aws-website

This is a wesite that is hosted & run on Amazon Web Services using a commonly established workflow.

# The following resrouces are used:

-EC2 (Elastic Cloud Computing) running Ubuntu Apache Web server

-ASG (Auto Scaling Group)

-ALB (Application Load Balancer)

-AWS Route 53

-AWS Certificate Manager


<img width="960" alt="webServer-EC2" src="https://github.com/Semir-Devops/aws-website/assets/144611511/78daad46-766c-4bcf-bf65-46db926f4526">

<img width="931" alt="Launch-template" src="https://github.com/Semir-Devops/aws-website/assets/144611511/b1dec0ce-607e-4485-8ee2-c3677672fed2">

The EC2 Instance (former screenshot) is created using a Launch Template (latter screenshot) as part of an ASG that will be triggered to match internet traffic (increase Virtual servers or decrease virtual servers)

<img width="949" alt="webServer-ASG" src="https://github.com/Semir-Devops/aws-website/assets/144611511/b371e2bd-d979-49bc-b9b2-14705aef6119">

The ASG is configured to have a maximum capacity of 3 EC2 instances in the case of traffic increase during client use & is what created the first EC2 instance seen above.

