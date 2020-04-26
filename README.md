# start-aws-instance

A very rough and ready script for starting, SSH-ing to and stopping an AWS instance.

I use AWS for remote development in RStudio and VSCode and got bored of starting and stopping instances through the AWS console, copying DNS names etc. This script wraps some [boto3](https://aws.amazon.com/sdk-for-python/) functions.

## Usage

1. Make sure the script is executable and somewhere on your `$PATH`
2. Either
    * Set an environemnt variable called `$AWS_INSTANCE_ID` and run `start-aws-instance`, or
    * Run `start-aws-instance <instance-id>`
3. Once the instance is up and running, the URL for RStudio will be displayed (`http://[something].amazon.com/8787`)
4. The script gives you the option of `ssh`-ing into the instance
5. Once you exit the `ssh` command, either by calling `exit` from the remote server or answering `no` to the prompt, you will be asked whether you want to shut down the instance
