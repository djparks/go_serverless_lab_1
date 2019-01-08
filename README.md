# go_serverless_lab_1

Setup - A one-time good deal :-)

## Step 0. Setup AWS user (unless you want to use existing admin user or one with the needed permissions)
See https://serverless.com/framework/docs/providers/aws/guide/credentials/

### Create Access Keys with custom policy
See this gist: https://gist.github.com/ServerlessBot/7618156b8671840a539f405dea2704c8

### Save your API and secret!

### Install Amazon CLI
Windows: https://docs.aws.amazon.com/cli/latest/userguide/install-windows.html

Mac: https://docs.aws.amazon.com/cli/latest/userguide/install-macos.html

General: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html

I added my keys to a new profile named "serverless-agent"

(Note: Where you see `$ serverless`, you can use `$ sls` instead as a shorthand.)

### Configure serverless to use these keys and secret
`$serverless config credentials --provider aws --key XYZ --secret abcd1234 --profile serverless-agent`

## Step 1. Install serverless globally
`$ npm install serverless -g`

## Step 2. Login to your serverless account
`$ serverless login`

## Step 3. Create a serverless function
`$ serverless create --template hello-world`

## Step 3b. Add serverless configuration
`$serverless config credentials --provider aws --key XYZ --secret abcd1234 --profile serverless-agent`

## Step 4. deploy to cloud provider
`$ serverless deploy`

## Your function is deployed. Let's invoke it:
`$serverless invoke -f hello`
