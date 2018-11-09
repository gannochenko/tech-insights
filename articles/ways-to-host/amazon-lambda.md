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

Q: What if I can not see in the console the function I have just deployed?
A: Go and switch the server you are currently on, for example, from us-east-2 (Ohio) to us-east-1 (N. Virginia)
