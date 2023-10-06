# aws-website

This is a wesite that is hosted & run on Amazon Web Services using a commonly established workflow.

# The following resrouces are used:

-EC2 (Elastic Cloud Computing) running Ubuntu Apache Web server

-ASG (Auto Scaling Group)

-ALB (Application Load Balancer)

-AWS Route 53

-ACM (AWS Certificate Manager)
<hr/>

The EC2 Instance (former screenshot) is created using a Launch Template (latter screenshot) as part of an ASG that will be triggered to match internet traffic (increase Virtual servers or decrease virtual servers).

<img width="960" alt="webServer-EC2" src="https://github.com/Semir-Devops/aws-website/assets/144611511/78daad46-766c-4bcf-bf65-46db926f4526">

<img width="931" alt="Launch-template" src="https://github.com/Semir-Devops/aws-website/assets/144611511/b1dec0ce-607e-4485-8ee2-c3677672fed2">


<hr/>

The ASG is configured to have a maximum capacity of 3 EC2 instances in the case of traffic increase during client use & is what created the first EC2 instance seen above.


<img width="949" alt="webServer-ASG" src="https://github.com/Semir-Devops/aws-website/assets/144611511/b371e2bd-d979-49bc-b9b2-14705aef6119">

<hr/>

An ALB is also created and attached to the EC2 instances & is configured with the SSL certificate created on AWS to direct traffic in a manner that won't stress the virtual server & to encrypt all traffic through HTTPS. 
The third screenshot specifies the association of the ALB to the SSL certifiate.

<img width="956" alt="webserver-ALB" src="https://github.com/Semir-Devops/aws-website/assets/144611511/516f164f-3599-41af-830c-688318fa7fd9">

<img width="946" alt="webServer-SSL" src="https://github.com/Semir-Devops/aws-website/assets/144611511/3183efc9-1298-4bd3-a323-24e33d4c4db7">

<img width="949" alt="webServer-ACM-ALB" src="https://github.com/Semir-Devops/aws-website/assets/144611511/f43a44cf-9eaf-41e2-a5a8-dfc2ada0d81e">

<hr/>

The final step is to jump to AWS Route 53 which will allow us to create a record with the domain name specified in the ACM.
Below is the A-record that is created on Route 53 in the hosted zone that is created upon domain name registration & the website created 

"semir-devops.com"

<img width="915" alt="Route53-Arecord" src="https://github.com/Semir-Devops/aws-website/assets/144611511/433869d5-df39-42ff-b5e3-88c2106fbabb">

<img width="959" alt="semir-devops-https" src="https://github.com/Semir-Devops/aws-website/assets/144611511/4c6647c7-0ae0-4d37-ba22-9bb68fc9c88e">

<hr/>
