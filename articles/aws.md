# AWS

Instead of traditional way of doing infrastructure by our own, AWS offers us a ready-to-go infrastructure, which automatically scales itself and in which you pay as you go. You do not over- or under-provisioning with AWS.

Resources like JS and CSS - S3 service (Simple Storage Service)
* REST API - [API service](https://docs.aws.amazon.com/apigateway/index.html#lang/en_us) ([Pricing](https://aws.amazon.com/ru/api-gateway/pricing/))
* Backend code - Lambda service
* Data - DynamoDB service
* Auth - Cognito service
* DNS - Route53 service
* Cacheing - CloudFront
* Account security - [IAM service](https://docs.aws.amazon.com/en_us/IAM/latest/UserGuide/introduction.html)

We can set up everything, using the following options:
* Web interface
* [CLI tool](https://docs.aws.amazon.com/cli/latest/reference/)
* Cloud Formation

## API Gateway service

* API - your endpoints
* Usage plan - specify restrictions, rate limits, monthly limits, bursts and so on
* API keys - create your API key and optionally attach it to Usage plans
* Custom domain names - allows to replace a default technical domain with some other domain of your own
* Client certificates - ???

## IAM service

Manages permissions of different people (developers, managers, etc.) or services.

