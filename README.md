# How to create and run an EMR cluster using AWS CLI
### A clear, easy-to-follow tutorial for beginners

---
The nice write-up version of this tutorial could be found on [my blog post on Medium](https://medium.com/@tranhnnguyenvn/how-to-create-and-run-an-emr-cluster-using-aws-cli-3a78977dc7f0?source=friends_link&sk=eca90ab3f969835f8c5ea221a536db0f "EMR cluster using AWS CLI")

## Motivation for this tutorial

I did spend many hours struggling to create, set up and run the Spark cluster on EMR using AWS Command Line Interface, AWS CLI. Although there are a few tutorials for this task that I found or were provided through courses, most of them are so frustrating to follow. Some are not clear enough; some miss some crucial steps; or assume the leaners know some prior knowledges about AWS, CLI configurations, etc. After successfully setting up and get the cluster running, I realized that this task is actually not that complicated; and we should get it done with ease. I don't want to see people struggling with this anymore. Therefore, I decided to make this tutorial.
This post is for someone who already has some knowledge about Spark, AWS, and specifically, who already know why they create the Spark cluster :). For more about Spark, please read the references here. 

### This is a long and detail tutorial. In brief, all the steps include:

Create an AWS account
Create an IAM user
Set up credentials in EC2
Create a S3 bucket to store log files produced by the cluster
Install AWS CLI package awscli
Set up AWS CLI environment (create the credentials and config files)
Create EMR cluster
Allow SSH Access
Create an SSH connection with the master node of the cluster
Start using the EMR cluster

Please feel free to skip any steps that you already know. 


### Some cautions: 
1. For this tutorial, AWS regular account should be used instead of AWS Educate account. The AWS regular account provides users the full access to AWS resources and IAM roles; while educate account has some limited access.
2. This is your responsibility for monitoring usage charges on the AWS account you use. Remember to terminate the cluster and other related resources each time you finish working. I have implemented the EMR cluster many times; and this tutorial should produce no cost or cost less than $0.5 on AWS.
3. The AWS console is subjected to change/upgrade through time, so I would recommend you to search AWS site for any updated tutorials/guidelines. This tutorial was generated according to AWS console in July, 2020.
4. This tutorial is produced using Chrome and Mac OS X. It should not be so much different on Windows platform.

### Reference
Some of the materials are from the Data Engineer nanodegree program on Udacity.



---
