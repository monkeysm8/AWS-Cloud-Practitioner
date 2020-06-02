# Architecting the Cloud - Best Practices

## Why Cloud Computing?

* IT assets becoming programmable resources
* Global availability and unlimited capacity
* High-level managed services, incl call center functionality, text to voice, machine learning, etc
* Security built in \(AWS manages security\)

## Design Principles - Scalability

1. Scale Up - Start with a small virtual machine and increase size
2. Scale Out - Start with an elastic load balancer, add more virtual machines as your project gets bigger
   1. Stateless Applications - Lambda \(no state is stored\)
   2. Stateless Components - Instead of storing state on server, it stores state on cookies on user's browser
   3. Stateful Components - Can store some stuff with databases that can scale with you \(add replicas or increase size\)
   4. Distributed Processing - Break your data into pieces and have EC2 instances work on them separately in parallel \(Elastic MapReduce\)

## Design Principles - Disposable Resources

* Treat your services like cattle, not pets
* If a server dies, just replace with another one
  1. Bootstrapping - Scripts allow you to set up an instance automatically, setup Apache
  2. Golden images - Take an Amazon Machine Image \(AMI\) and use it for autoscaling
  3. Hybrid of the two

## Design Principles - Infrastructure as Code

* Cloudformation
* Allows you to deploy infrastructure to many clients very easily without manually setting anything up

## Design Principles - Automation

* Use alarms, events to automate creation/maintenance of infrastructure
* Loose coupling: Make sure failure in one component doesn't affect other pieces of infrastructure
  * Well defined interfaces: Use RESTful API
  * Service discovery: Don't use fixed IP addresses. Instead use DNS names/endpoints.
  * Asyncronous integration: Messages \(actions\) remain in queue so if one EC2 goes down, the actions are stored in queues for the next EC2 to pick up
  * Graceful failure: If something breaks, nicely tell the user and report to developers

## Design Principles - Serverless not services

* Managed Services \(other companies like Paypal\)
* Serverless Architectures \(Lambda, DynamoDB, etc\)

## Design Principles - Databases

* Relational: Aurora
  * High scalability
  * High availability \(6 copies of data at any given time\)
  * Data needs joins or complex transactions
* Nonrelational: DynamoDB
  * High scalability
  * High availability
  * Data does not need joins or complex transactions
* Data Warehouse: Red Shift
  * Meant for data for business analysis
  * Red Shift is highly scalability and available
  * Red Shift not meant for online transaction processing \(not production database\)

## Design Principles - Search

* Cloud Search or Elastic Search
* Cloud search: less control, easier
* Elastic search: more control
* Both are very scalability

## Design Principles - Misc

* Remove single points of failure, everything should have redundancy
* Detect failure with monitoring \(Health checks\)
* Durable data storage
  * Don't store all on an EC2 instances
  * Store instead in S3 or Dynamo
* Automate multi-center resilience \(multiple Availability Zones\)
* Introduce fault isolation and horizontal scaling

## Design Principles - Financial

* Optimize for cost
  * Elasticity: More servers when busy, less when not busy with auto scaling
  * Purchasing options:
    * Reserved Capacity
    * Spot Instances

## Design Principles - Caching

* Application Caching
* Edge Caching

## Design Principles - Security

* Offload security to AWS
* Reduce privileged access
* Treat security as code

## 

