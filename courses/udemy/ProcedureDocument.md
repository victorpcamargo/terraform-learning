# Procedure Document
### Instructor: Edward Viaene

## Github repository
- https://github.com/wardviaene/terraform-course
- Use the download button on the Github website (zip) or git clone this repository

## AWS Setup
- There is a lecture on how to setup AWS, here are some notes to clarify the setup
- Make sure you have installed the AWS CLI
    - if you use my vagrant devops-box it is included by default
    - otherwise you can download it manually from https://aws.amazon.com/cli/
    - If you're on linux you can also use "sudo pip install --upgrade awscli"
        - If you don't have pip, try sudo apt-get install python-pip
    - There is a lecture on how to add an admin user, this need to be done to create an access key and secret key
    - Use "aws configure" to enter the keys
        - you can optionally specify a default region - but no worries, in terraform you can set any region you want
        - Use http://www.cloudping.info/ to determine your region
    - You can test whether it works by entering: aws iam get-user
        - This will also show your AWS userid which you need afterwards

## Useful Commands
$ terraform plan                                  # plan

$ terraform apply                                 # shortcut for plan & apply - avoid this in production

$ terraform plan -out out.terraform      # terraform plan and write the plan to out file

$ terraform apply out.terraform            # apply terraform plan using out file

$ terraform show                                  # show current state

$ cat terraform.tfstate                           # show state in JSON format

## Using putty instead of the ssh command
The course is explained using MacOS/Linux. If you rather want to use putty, use the following steps to create your SSH keypair:

1. Download Putty and PuttyGen from http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
2. Launch PuttyGen and click the "Generate" button to generate a new public/private key
3. You can enter a passphrase or leave it blank
4. Save the public and private keys by clicking the Save public key and Save private key buttons

## Reference Documentation
- Download URL: https://www.terraform.io/downloads.html
- AWS Resources: https://www.terraform.io/docs/providers/aws/
- List of providers: https://www.terraform.io/docs/providers/index.html
- List of AMIs for ubuntu: https://cloud-images.ubuntu.com/locator/ec2/ (hint: make sure not to pick arm64 if you're on amd64)

