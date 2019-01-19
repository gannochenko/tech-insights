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
    * Resources
        * Nothing will go live until we select "Deploy"
        * Request-response cycle
            * Method request allows to validate the request
            * Integration request allows to connection request to a consumer service, like lambdas or other
            * Integration response allows to re-format the response from the consumer service
            * Method response is also used to shape the response
        * If we create a new resource:
            * Configure as proxy resource - this resource will be a default one, serving all verbs
            * Enable API Gateway CORS - enable CORS with damn pre-flights
            * Use Lambda Proxy integration - means that lambda will receive the whole request as the first argument, not only its body
            * Body mapping template is used to transform the request/response body, in order to make it suitable for the attached request consumer
                * https://docs.aws.amazon.com/en_us/apigateway/latest/developerguide/api-gateway-mapping-template-reference.html
    * Stages - dev or prod or anything else
    * Authorizers - apply authorization for endpoints
    * Models - defines a shape of the data the API operates with, we can:
        * validate the input against a model we define
        * use it in Body mapping template
        * See more at https://json-schema.org/understanding-json-schema/index.html
* Usage plan - specify restrictions, rate limits, monthly limits, bursts and so on
* API keys - create your API key and optionally attach it to Usage plans
* Custom domain names - allows to replace a default technical domain with some other domain of your own
* Client certificates - ???

## IAM service

By default, no service has access to other services.

Manages permissions of different people (developers, managers, etc.) or services.
There is always a root user - account owner.

When create a user, there are two access options:
* Management console
* Programmatic access

We can add user to a group (preferable) or attach a chosen policy directly.

Always enable MFA
Always apply an IAM password policy

Don't get users more permissions than they want.

## ???

## Questions

* Read more about KMS
    * https://docs.aws.amazon.com/en_us/kms/latest/developerguide/getting-started.html
    * https://www.matchilling.com/storing-security-sensitive-data-using-aws-kms-and-openssl/
* Read more about secrets
* Think of how to disable pre-flights
    * https://medium.com/@praveen.beatle/avoiding-pre-flight-options-calls-on-cors-requests-baba9692c21a

## Listings

### Sample schema

```json
{
    "$schema": "http://json-schema.org/draft-04/schema",
    "title": "CompareData",
    "type": "object",
    "properties": {
        "age": {"type": "integer"},
        "height": {"type": "integer"},
        "income": {"type": "integer"}
    },
    "required": ["age", "height", "income"]
}
```
