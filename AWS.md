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



24-04-24

DynamoDb
File System in the Cloud