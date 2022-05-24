# Access AWS S3 Bucket with AWS CLI
Pulling data from AWS S3 Bucket with two lines of code using AWS Command Line Interface (CLI)

## Step 1
### installing or updating AWS Command Line Interface (AWS CLI)
run the msiexec command to run the MSI installer (Window)
> msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi

## Step 2 
### Confirm Installation, check AWS CLI version
run command
> aws --version
>> output sample: aws-cli/2.4.5 Python/3.8.8 Windows/10 exe/AMD64 prompt/off

## Step 3 
### setting up new configuration 
> aws configure
> AWS Access Key ID [None]: <your access key id>
> AWS Secret Access Key [None]: <your secret access key>
> Default region name [None]: us-west-1
> Default output format [None]: json

## Step 4 
### check list of files in a specific bucket/folder
>aws s3 ls s3://YOUR_BUCKET/YOUR_FOLDER/ --recursive --human-readable --summarize

## Step 5 
### from the list of files in the folder, copy the file name and replace here
### copying a file from a bucket to a local file (out file name after the path)
> aws s3 cp s3://YOUR_BUCKET/YOUR_FOLDER/<fileName.fileType> <fileNameCopy.fileType>

**Only do step 1-3 once(the 1st first time) after that only follow step 4 and 5.
