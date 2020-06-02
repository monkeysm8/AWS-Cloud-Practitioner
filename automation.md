# Automation

## Autoscaling

* Review: EC2 connects to one database that is duplicated to a second database \(redundancy\).
* No redundancy on the EC2 itself. Autoscaling group will fix this.
* You can set up how many instances you want with Autoscaling. When one fails, it will automatically create a new one
* You can set a startup script to run when each new instance starts

## Route 53

* Amazon's DNS service
* Domain registration

## Elastic Beanstalk

* Allows you to deploy everything \(provisions everything like EC2 and RDS and everything else\) all at one button
* Creates load balancers, auto-scaling groups, security groups, etc.
* Provisioning EC2 instances, installs PHP

## CloudFormation

* Way of scripting out infrastructure
* Turning infrastructure into code
* Codify creating EC2 instances, security groups, etc
* JSON that describes your cloud environment - this is a template
* Elastic Beanstack and CloudFormation are free, but you pay for the resources that are provisioned as a result of using EB and CF

