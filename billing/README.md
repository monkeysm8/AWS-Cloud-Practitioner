# Billing

## Philosophy on pricing

Pay for what you use, start or stop using product at any time. 

* No long-term contracts required.
* Free Tier to help new AWS users get started

### Pricing policies

* \*\*Pay as you go: \*\*EC2 used to be pay by hour, pay by second as it's used
* **Pay less when you reserve:** If you reserve time ahead of time, you get a discount
* \*\*Pay even less by unit when using more: \*\*If you use more, you pay less per GB
* **Pay even less as AWS grows**
* Custom pricing for enterprise

### What's free?

1. Amazon VPC
2. Elastic Beanstalk \(services it provisions are not free\)
3. CloudFormation \(services it provisions not free\)
4. Identity Access Management \(IAM\)
5. Auto Scaling \(EC2 instances it uses are not free\)
6. OpsWorks
7. Consolidated Billing \(add all AWS accounts into one bill\)

### 3 Fundamental Charges

1. Compute
2. Storage
3. Data Out to Internet \(Data In is free\)

### What determines price?

1. Clock hours of server time \(time server is running\)
2. Machine configuration \(more resources consumed = more paid\)
3. Machine purchase type \(some instance types cost more\)
4. Number of instances
5. Load balancing
6. Detailed monitoring \(monitor EC2 by minute instead of 5-min intervals\)
7. Auto scaling \(EC2 instances cost money\)
8. Elastic IP Addresses
9. Operating systems \(Windows\) and software packages

* Elastic Compute Cloud can reserve instances ahead of time, even cheaper if you pay upfront

## S3 - What determines price?

1. Storage class \(Standard or IA\)
2. Storage amount
3. Number of requests
4. Data transfer \(data transfer out\)

## RDS - What determines price?

1. Number of hours RDS is running
2. Database characteristics \(licensed?\)
3. Database purchase type \(huge, nano?\)
4. Number of instances
5. Provisioned storage \(how big?\)
6. Requests made to database
7. Deployment type \(multi A-Z, read replicas\)
8. Data transfer out

## Cloudfront - What determines price?

1. Traffic distribution
2. Requests
3. Data transfers out

## Exam Tips

* Consolidated billing allows you to get volume discounts for all your accounts
* Unused reserved instances for EC2 are applied across group
* CloudTrail is on per-account and per-region basis , can be aggregated into single bucket in paying account

