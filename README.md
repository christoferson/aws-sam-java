# AWS Serverless Application Model (SAM) in Java 11

## sam-java-basic

Basic project with 1 Lambda Function behind an Api Gateway

## 002 sam-java-rest

Project with individual Lambda Functions for REST service behind an Api Gateway

Layer - Does not use later, each unique CodeURI will create a separate archive to upload.

# Todo

- [ ] Implement Stage for Dev,Staging,Production

- [ ] Implement Layers

- [ ] Implement Lambda Versions/Alias



### Errors

- Problem: sam deploy: Error: Security Constraints Not Satisfied!
  
  Cause: You need to explicitly say yes for "PetStoreFunction may not have authorization defined, Is this okay? [y/N]:"
  
```
sam deploy --guided

Configuring SAM deploy
======================

Looking for config file [samconfig.toml] :  Not found

Setting default arguments for 'sam deploy'
=========================================
Stack Name [sam-app]: awslabs-springboot-petstore
AWS Region [eu-west-1]:
#Shows you resources changes to be deployed and require a 'Y' to initiate deploy
Confirm changes before deploy [y/N]: y
#SAM needs permission to be able to create roles to connect to the resources in your template
Allow SAM CLI IAM role creation [Y/n]: Y
#Preserves the state of previously provisioned resources when an operation fails
Disable rollback [y/N]: N
PetStoreFunction may not have authorization defined, Is this okay? [y/N]:
Error: Security Constraints Not Satisfied!
```


### Resources

- https://aws.amazon.com/jp/blogs/aws/new-accelerate-your-lambda-functions-with-lambda-snapstart/

- https://github.com/awslabs/aws-serverless-java-container/tree/main/samples/springboot2/pet-store

