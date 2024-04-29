## AWS set up 

Create EC2 instance 
Create s3 bucket 
change EC2 instance type

## Virtual Private Cloud 

*It's an our own private server on AWS cloud
*It required IP adresses ,Subnets, Avaibility Zones

22-04-2024 task's - 
*create repositories and granted access to the team members
*Create Schema in the RDS SQL server Database named as Vedbhoomi
*Get Access to Aws account
*log in to AWS and set up for MultiFactor Authentication 
*Get to know about What is RDS how is created 
*Create VPC (virtual private clouds)
*Create Routes and Subnets 
*Change Secuirity Group port 

Today I am going to learn 
Aws calculator
Different databse services
Lambda
what are application Services in aws
Create a VM and Install SQL Express on it
Some basic knowladge of Custom domains

aplifier 
lamda
create CI/CD on AWS


.gitlab-ci.yml

stages:
  - build_stage
  - deploy_stage

build:
  stage: build_stage
  image: node
  script:
  #  - apt update -y
  #  - apt install npm -y 
    - npm install 
  artifacts:
    paths:
      - node_modules
      - packge-lock.json

deploy:
  stage: deploy_stage
  image: node
  script:
  #  - apt update -y
  #  - apt install nodejs -y
    - node app.js > /dev/null 2>&1 &



PipeLine

!! AWS has Code build and CodeDeploy server for automation



## AWS free tier services ##

** Services that are available in the AWS Free Usage Tier

  -750 hours of  Amazon EC2  Linux or RHEL or SLES t2.micro instance usage (1 GiB of memory and 32-bit and 64-bit platform support) – enough hours to run continuously each month
  
  -750 hours of an  Elastic Load Balancer  plus 15 GB data processing
  
  -750 hours of  Amazon RDS  Single-AZ Micro DB Instances, running MySQL, MariaDB, PostgreSQL, Oracle BYOL or SQL Server Express Edition – enough hours to run a DB Instance continuously each month. You also get 20 GB of database storage and 20 GB of backup storage
  
  -750 hours of  Amazon ElastiCache  Micro Cache Node usage – enough hours to run continuously each month.
  
  -30 GB of  Amazon Elastic Block Storage  in any combination of General Purpose (SSD) or Magnetic, plus 2 million I/Os (with EBS Magnetic) and 1 GB of snapshot storage
  
  -5 GB of  Amazon S3  standard storage, 20,000 Get Requests, and 2,000 Put Requests
  
  -25 GB of Storage, 25 Units of Read Capacity and 25 Units of Write Capacity, enough to handle up to 200M requests per month with  Amazon DynamoDB 
  
  -25  Amazon SimpleDB  Machine Hours and 1 GB of Storage
  
  -1,000   Amazon SWF   workflow executions can be initiated for free. A total of 10,000 activity tasks, signals, timers and markers, and 30,000 workflow-days can also be used for free
  
  -100,000 Requests of  Amazon Simple Queue Service 
  
  -100,000 Requests, 100,000 HTTP notifications and 1,000 email notifications for  Amazon Simple Notification Service  
  
  -10  Amazon Cloudwatch  metrics, 10 alarms, and 1,000,000 API requests
  
  -50 GB Data Transfer Out, 2,000,000 HTTP and HTTPS Requests for  Amazon CloudFront 
  
  -15 GB of bandwidth out aggregated across all AWS services


## 12 Months free


  -Amazon EC2: 750 hours per month of Linux, RHEL, or SLES t2.micro / t3.micro instance usage or 750 hours per month of Windows t2.micro / t3.micro instance usage dependent on Region.

  -Amazon Simple Storage Service (Amazon S3): 5 GB of Amazon S3 standard storage, 20,000 GET requests, and 2,000 PUT requests.

  -Amazon Relational Database Service (Amazon RDS): 750 hours of Amazon RDS Single-AZ db.t2.micro, db.t3.micro, and db.t4g.micro instances usage for running MySQL, PostgreSQL, MariaDB, or db.t2.micro instance usage running SQL Server (running SQL Server Express Edition); 20 GB of general purpose SSD database storage and 20 GB of storage for database backup and database snapshots.

  -Amazon CloudFront: 50 GB data transfer out and 2,000,000 HTTP and HTTPS requests each month.


## Always free


    Amazon DynamoDB: Up to 200 million requests per month (25 write capacity units (WCUs) and 25 read capacity units (RCUs)); 25 GB of storage.

    Amazon S3 Glacier: Retrieve up to 10 GB of your Amazon S3 Glacier data per month for free (applies to standard retrievals using the Glacier API only).

    AWS Lambda: 1 million free requests per month; up to 3.2 million seconds of compute time per month.


Link to get to know about free tiers in aws : https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=tier%2312monthsfree&awsf.Free%20Tier%20Categories=*all