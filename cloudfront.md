# CloudFront

Amazon's CDN network, used to deliver:

* Entire website, including dynamic, static, streaming, and interactive content using edge locations
* Requests for content automatically routed to nearest edge location so content is delivered with best performance possible 



## Content Delivery Network \(CDN\)

* System of services around the world that deliver web pages or web page content to a user based on user geographic location, origin of the webpage, and content delivery server 
* Works with origin types listed below Also works with non-AWS origins 

## Edge Location  

* Where content will be cached Similar to AWS Region/AZ 
* As close to user as possible 

## Origin 

* Origin of files that CDN will distribute:

  * S3 bucket
  * EC2 instance
  * Elastic Load Balancer
  * Route53 

## Distribution

Name given to the CDN which consists of a collection of edge locations

The first time a user goes to a website, it'll:

* Check a local edge location to see if website asset is there
* If not, it will download the asset from the origin and cache it to the edge location
* Next time someone tries to access, they will get the cached version from a local edge location
* Reduces stress on web servers and increases speed to download large files

Distribution Types  

* Web distribution - Used for websites 
* RTMP - Used for media streaming 

## Setting up CloudFront 

1. Choose Web distribution 
2. Origin Domain Name: Choose an S3 bucket 
3. Origin Path: You can choose subdirectories for your origin 

Once it's deployed, you will see a domain name. Use that and the name of a file in your bucket to access. 

## Exam Tips 

* Content comes from Origin 
* Cached at a local Edge Location 
* Takes awhile for the first person to access, much quicker every time after that because it's cached geographically close to you

