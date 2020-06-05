# Elastic Cloud Compute \(EC2\)

* EC2 is compute-based, it's not serverless. It is a server! 
* Use private key to connect to EC2 
* Security groups are virtual firewalls in the cloud. Need to open ports in order to use them \(22 for SSH, 80 for HTTP, 443 for HTTPS, 3389 for RDP\) 
* Always design for failure, have one EC2 instance in each availability zone \(AZ\)



### Placement groups 

These are logical grouping of instances in one of the following configurations:

* A cluster placement group is a logical grouping of instances within a single Availability Zone. Cluster placement groups are recommended for applications that benefit from low network latency, high network throughput, or both, and if the majority of the network traffic is between the instances in the group
* A spread placement group is a group of instances that are each placed on distinct underlying hardware. Spread placement groups are recommended for applications that have a small number of critical instances that should be kept separate from each other

