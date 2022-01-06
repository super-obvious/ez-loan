# Ez-loan backend 

## Notes

> - A/B testing is specifically required for testing of x2 user stories. 
> - There is an open [Amplify A/B Github issue](https://github.com/aws-amplify/amplify-console/issues/331) requesting this feature 

## Initial response

In the absence of native support for A/B testing in Amplify, the requirement can be met by combining AWS Codepipeline, CodeBuild, Lambda and StepFunctions. 

**Front End Pipeline** 

A front end workflow focused on A/B testing targeting mobile apps might include AWS Device Farm in the CI/CD pipeline.

If the A and B tests were maintained in different CodeCommit Branches, branch-based pushes can trigger a pipeline to deploy the A/B builds. 

**Back End Pipeline** 

Since the app seeks to use GraphQL, the recommendation would be to follow the AWS Prescriptive Guidance on GraphQL Architecture documented below with links to AWS blogs.

**Auth**

Auth can be done with AWS Cognito


## App Requirements

* CI/CD Pipeline
* Tests
* A/B 
* AWS GraphQL
* Auth
* Mobile

## Requirements met by

* AWS CDKPipelines, CodeCommit, CodeBuild, Lambda, StepFunctions, CloudFormation
* AWS AppSync
* Amplify + Local Mocking with GraphiQL IDE
* AWS Cognito & Lambda
* AWS Device Farm

## Frontend Pipeline Arch

For frontend, split the pipeline documented below, with two CodeBuild parrallel phases based on CodeCommit branch

> [CI/CD for Mobile Apps on AWS](https://catalog.us-east-1.prod.workshops.aws/v2/workshops/cc4e013e-6779-4574-9672-ff201b76282d/en-US/architecture)


## Backend Pipeline Arch

For backend, follow the AWS Prescriptive Guidance on GraphQL Architecture

> [Set up CI/CD for AWS AppSync GraphQL API updates](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/set-up-ci-cd-for-aws-appsync-graphql-api-updates.html)

![AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/images/pattern-img/6825c955-58b4-48b2-b022-a36f92ba663a/images/471eb45e-2573-483c-bb9b-3a72e0543cff.png)

![Stack update architecture](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/images/pattern-img/6825c955-58b4-48b2-b022-a36f92ba663a/images/cf50d28e-6d9d-451b-a5bc-c727b4de4657.png)

## Resources

* [Build with GraphQL](https://aws.amazon.com/blogs/mobile/building-scalable-graphql-apis-on-aws-with-cdk-and-aws-appsync/)
* [Amplify local mocks](https://aws.amazon.com/blogs/mobile/amplify-framework-local-mocking/)
