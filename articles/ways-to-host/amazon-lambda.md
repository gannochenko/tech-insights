# Amazon lambda

Put something heavy or seasonal there.

## [Serverless](https://serverless.com/)

Serverless means that you don't need to worry about how to scale your server, but you still need one :)

~~~~
npm install serverless -g
sls create -t aws-nodejs
sls config credentials --provider aws --key ACCESS_KEY_FROM_AWS --secret SECRET_FROM_AWS
sls deploy
sls invoke --function FUNCTION_NAME
sls invoke local --function FUNCTION_NAME
~~~~
