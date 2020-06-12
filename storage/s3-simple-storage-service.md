# S3 \(Simple Storage Service\)

## Overview

* Provides developers and IT teams with secure, durable, highly-scalable object storage
* Safe place to store your files
* Object-based storage \(pictures, Word files, videos\), not operating system or database
* **Objects can be anywhere from 0 bytes to 5 TB in size**
* Unlimited storage, but you pay by the gig
* Files are stored in buckets
* Bucket is a folder in the cloud
* Buckets are universal namespace. Must be unique globally.
* URL looks like https://s3-eu-west-1.amazonaws.com/stuff
  * Region + Region \# + amazonaws.com + bucket name

## Data Consistency Model

* Read after Write consistency for PUTS of new objects

  * You can read a file as soon as you have uploaded it.

* Eventual consistency for overwrite PUTS and DELETES \(can take some time to propogate\)
  * If you update a file and overwrite the old version, you may get the old file or the new file. It will eventually show up.
  * You may be updating to one availability zone, may take time to propagate to other availability zone

## S3 Key-Value Store

**S3 is object based, objects consist of:**

* Key \(name of object, e.g. hello.txt
* Data in file \(sequence of bytes\)
* Version ID \(important for versioning\)
* Metadata \(data about data, e.g. tags\)
* Subresources:
  * Access Control List
  * Torrents

## Useful Information

* Built for 99.99% availability
* Amazon guarantees 99.99999999999% \(11 x 9s\) durability

  * If you upload x amount of files, 99.99999999999% of those files will actually be uploaded \(you won't lose any files\) 

* Tiered storage availability 
* Lifecycle management

  * If a file is over 30 days old, move it from one storage tier to another and eventually archive to Glacier 

* Versioning

  * Multiple versions of a file 

* Encryption
* Secure data with Access Control Lists and Bucket Policies
  * Bucket policies: Policy is for a specific bucket
  * ACL: Individual file level, control who can access a specific file

## S3 Storage Tiers/Classes



**S3 Standard**

* 99.99% availability
* 99.99999999999% durability
* Stored redundantly across multiple devices \(multiple disks\) and multiple facilities \(multiple availability zones\)
* Designed to sustain loss of 2 facilities concurrently

**S3 - IA \(Infrequently Accessed\)**

* Data accessed less frequently but requires rapid access when needed
* Lower fee than Standard but charged a retrieval fee

**S3 One Zone - IA**

* Same as S3 - IA but do not require multiple availability zone data resilience
* Only stored in one availability zone

**Glacier**

* Used for archival only
* Cheapest
* Expedited, standard, or bulk

  * Expedited: Restored within few mins, high fee
  * Standard: 3-5 hours for restore
  * Bulk: 5-12 hours

  **N.B. No retrieval fee for Standard**

## S3 - Charges 

Charged for:

* Storage
* Requests
* Storage management pricing

  * Tags that define who owns an object

* Data transfer pricing 

  * Transferring from one region to another

* Transfer acceleration
  * Fast and easy secure transfers across long distances

## S3 Transfer Acceleration

* Users upload to an edge location instead of directly to S3 bucket
* Once it goes to an edge location, it automatically gets distributed to the S3 bucket
* File goes across Amazon's backbone to transfer much faster

## S3 for Web Pages 

* S3 can host static web pages \(not dynamic like Wordpress or PHP\) 
* It will scale automatically, will scale with demand. Useful for large number of requests. 
* You can use bucket policies to make an entire bucket public \(used for static websites\)

