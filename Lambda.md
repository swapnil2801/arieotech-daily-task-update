## Lambda function creation and diploy ##

1. Search lambda function on Aws.
2. Create new lambda function
3. test it
4. Create new layer
5. Upload packges zip file.
6. I have used python as script language and use requests package to create http request. 
   So, i need install requests in my project folder. And then zipped the folder with name 'pypackages'.
   for install command used - pip3 install requests -t .

7. Create new layer and upload packges zip file.
8. select version and done test it.
9. Diploy to API gateway 
10. Create rest API new
11. Add name and description
12. Create any method in it like get ,post etc add lambda funtion name and test it.
13. Enable cors and deploy it.
14. Create stage and done.
15. For testing use postman or click on link open the data in browser.
16. Add trigger in Lambda.

## Direct diploy from GitLab 

1. Add the lambda file in project directory.
2. Create user in AWS and add Acsess key and secret access key in Gitlab variables
3. Inside .yml file write deploy script to deploy lambda function to AWS like
e.g

stages:
  - deploy

variables:
  LAMBDA_FUNCTION_NAME: "your-lambda-function-name"
  AWS_REGION: "your-aws-region"
  AWS_ACCESS_KEY_ID: $AWS_ACCESS_KEY_ID
  AWS_SECRET_ACCESS_KEY: $AWS_SECRET_ACCESS_KEY

deploy_lambda:
  stage: deploy
  image: amazon/aws-cli
  script:
    - aws lambda create-function --function-name $LAMBDA_FUNCTION_NAME --runtime python3.8 --handler lambda_function.lambda_handler --role arn:aws:iam::YOUR_ACCOUNT_ID:role/YOUR_ROLE_NAME --zip-file fileb://lambda_function.zip --region $AWS_REGION
  only:
    - master

4.After this commit the changes and run the pipeline the lambda function get deploy easily.