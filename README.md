# Terraform-to-mount-efs-to-ec2-

##
# **Read Me**

This Terraform configuration file creates an Amazon Web Services (AWS) Virtual Private Cloud (VPC) and deploys an EC2 instance in the VPC with a private SSH key. It also creates a public subnet with an internet gateway, a route table, an S3 bucket, and an Elastic File System (EFS) with a mount target.

## **Prerequisites**

- An AWS account and an AWS access key and secret key pair
- Terraform installed on your local machine

## **Usage**

1. Clone the repository to your local machine and navigate to the project directory.
2. Run terraform init to initialize the Terraform project.
3. Set the AWS access key and secret key environment variables by running export AWS\_ACCESS\_KEY\_ID=\<your\_access\_key\> and export AWS\_SECRET\_ACCESS\_KEY=\<your\_secret\_key\> in your terminal or by setting them in your IDE.
4. Run terraform apply to create the resources in your AWS account. You will be prompted to confirm the creation of the resources before they are created.
5. After the command completes successfully, the EC2 instance will be deployed and you can connect to it using the private key generated in the project directory.

## **Resources Created**

- An AWS VPC with a CIDR block of 10.0.0.0/16
- A public subnet in the VPC with a CIDR block of 10.0.1.0/24
- An internet gateway attached to the VPC
- A route table for the VPC with a default route to the internet gateway
- An S3 bucket with private access
- An EFS with a mount target in the public subnet
- An EC2 instance in the public subnet with a security group allowing SSH traffic

## **Inputs**

- aws\_access\_key - AWS access key ID
- aws\_secret\_key - AWS secret access key

## **Outputs**

- public\_ip - Public IP address of the EC2 instance created.

## **Author**

This Terraform configuration was created by Tatah Noel Limnyuy.