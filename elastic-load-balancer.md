# Elastic Load Balancer

Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as: 

* Amazon EC2 instances.
* Containers
* IP addresses
* Lambda functions

It can handle the varying load of your application traffic in a single Availability Zone or across multiple Availability Zones.

3 Types of Elastic Load Balancer

#### Application Load Balancer 

Application Load Balancer is best suited for load balancing of HTTP and HTTPS traffic and provides advanced request routing targeted at the delivery of modern application architectures, including microservices and containers. Operating at the individual request level \(Layer 7\), Application Load Balancer routes traffic to targets within Amazon Virtual Private Cloud \(Amazon VPC\) based on the content of the request.

#### Network Load Balancer <a id="Network_Load_Balancer"></a>

Network Load Balancer is best suited for load balancing of Transmission Control Protocol \(TCP\), User Datagram Protocol \(UDP\) and Transport Layer Security \(TLS\) traffic where extreme performance is required. Operating at the connection level \(Layer 4\), Network Load Balancer routes traffic to targets within Amazon Virtual Private Cloud \(Amazon VPC\) and is capable of handling millions of requests per second while maintaining ultra-low latencies. Network Load Balancer is also optimized to handle sudden and volatile traffic patterns.

#### Classic Load Balancer 

Classic Load Balancer provides basic load balancing across multiple Amazon EC2 instances and operates at both the request level and connection level. Classic Load Balancer is intended for applications that were built within the EC2-Classic network.

