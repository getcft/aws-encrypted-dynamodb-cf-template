# aws-encrypted-dynamodb-cf-template
[![Build Status](https://travis-ci.org/getcft/aws-encrypted-dynamodb-cf-template.svg?branch=master)](https://travis-ci.org/getcft/aws-encrypted-dynamodb-cf-template)

## Description:

This solution creates an [AWS DynamoDB](https://aws.amazon.com/dynamodb/) encrypted table with a primary key and sort key.

The AWS CloudFormation template creates a AWS DynamoDB encrypted example table that reflects a scenario where you have clients and invoices associated to those clients. The primary keys would be email address and the sort key would be invoices

Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-region, multi-master database with built-in security, backup and restore, and in-memory caching for internet-scale applications.

_***note AWS DynamoDB will incur costs**_

* [DynamoDB pricing](https://aws.amazon.com/dynamodb/pricing/) resource used in example: 1 Provisioned Write and 1 Provisioned Read Capacity Unit

## Prerequisites:

* AWS account and environment configured with AWS Credentials
* IAM user with AWSCloudFormationReadOnlyAccess, AmazonDynamoDBFullAccess

## See how it works:

AWS Management Console

* Login to AWS Management Console
* Launch in CloudFormation encrypted-dynamodb-cf-template.yml (from the repo you cloned)

CloudFormation Fields

* Stack name (Enter a name to associate to your AWS DynamoDB deployment)**Next**
* Continue choosing **Next**
* Click **Create**

## Test:

In the AWS Management Console under DynamoDB you should be able to verify the following have been created:

* 1 encrypted table named "Client_Invoice"
* 1 Provisioned Write and 1 Provisioned Read Capacity Unit
* Primary Key "client_email"
* Sort Key "invoice_number"
