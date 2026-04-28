# CloudTask Serverless SaaS Architecture

## 1. Project Overview

CloudTask is a multi-tenant serverless SaaS task management application built on AWS.

The system allows multiple companies/tenants to use the same application while keeping their data logically isolated.

## 2. Architecture Goals

- Build a secure multi-tenant SaaS application
- Use serverless AWS services to reduce operational overhead
- Support scalable API requests
- Store tenant-specific data securely
- Enable secure file uploads
- Add event-driven processing for future features
- Monitor logs, metrics, and failures

## 3. High-Level Architecture

```text
User
  |
  v
CloudFront
  |
  v
S3 Static Website - React App
  |
  v
Amazon Cognito
  |
  v
API Gateway
  |
  v
AWS Lambda
  |
  +--> DynamoDB
  |
  +--> S3 Attachments Bucket
  |
  +--> EventBridge
  |
  +--> CloudWatch
