# Overview
We decided to use AWS as our Cloud provider for the Free Software project. The motivation comes from the fact that for the Evaluation Package we rely on an Open Source software called [EvalAI](https://github.com/Cloud-CV/EvalAI) which works on AWS. Later (after MVP), the Cloud provider will be reassessed.

## Architecture
![End2End MVP (1).jpg](/.attachments/End2End%20MVP%20(1)-9cfb57d6-6288-48e4-bbbe-8004451702a8.jpg) 

### Cognito
Users authenticate using AWS Cognito service. They get a JWT token they use to get access to the required services. To use Cognito User Pools within your apps please refer to the documentation: [https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-integrate-apps.html](https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-integrate-apps.html).
The endpoint is secured by API keys and Cognito for user-level authentication and user-group authorization.

### S3 Bucket
To upload private datasets we use presigned S3 URL ([see here](https://docs.aws.amazon.com/AmazonS3/latest/dev/PresignedUrlUploadObject.html)). This mechanism is managed by a Lambda function available in the [AWS FHIR implementation](https://github.com/awslabs/fhir-works-on-aws-deployment).

### EKS Cluster
The EKS cluster is running with internet-facing access of the K8S API endpoints now with the EC2 cluster nodes in private subnets.

Autoscaling of EC2 cluster nodes is also already enabled and tested.
 
To connect, make sure you have latest AWS CLI v2 and kubectl installed, then configure the following AWS user for the AWS CLI:

>Please send your request to the Core Package Team to get access 

Next, execute following on the command line:


```
CLUSTER_NAME=ai4h-mvp-k8s-dev

aws eks --region eu-central-1 update-kubeconfig --name $CLUSTER_NAME

code ~/.kube/config

# -> make sure that path to aws binary is set, e.g. command: /usr/local/bin/aws

kubectl config use-context arn:aws:eks:eu-central-1:[ACCOUNT_ID]:cluster/$CLUSTER_NAME

kubectl get nodes
```

This should display the K8S EC2 cluster nodes. If it works you are connected and can deploy stuff.

 
We recommend to use Lens for getting a quick overview of the K8S cluster state and find it very helpful: [https://k8slens.dev/](https://k8slens.dev/)

### Cloud Front, API Gateway
The endpoint is hosted using API Gateway

### DynamoDB, Elastisearch
The database and storage layer consists of Amazon DynamoDB and S3, with Elasticsearch as the search index for the data written to DynamoDB

