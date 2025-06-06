# Architecture: AI Resume Reviewer & Job Matcher

## Overview
A serverless web app for resume analysis and job matching, built with AWS Free Tier and GPT-4o.

## Components
- **Frontend**: Next.js (TypeScript, Tailwind CSS) hosted on AWS Amplify.
- **API**: AWS API Gateway for routing requests to Lambda.
- **Backend**: AWS Lambda (Python 3.12) for resume processing and job matching.
- **Storage**: Amazon S3 for resume storage (encrypted).
- **Database**: Amazon DynamoDB for user data, feedback, and job listings.
- **Authentication**: Amazon Cognito User Pool for secure user management.
- **AI**: OpenAI GPT-4o API for resume analysis and skill extraction.
- **Monitoring**: AWS CloudWatch for logs and metrics.

## Data Flow
1. User logs in via Cognito (Next.js frontend).
2. User uploads resume to S3 via API Gateway and Lambda.
3. Lambda extracts resume text (PyPDF2) and sends to GPT-4o.
4. GPT-4o returns feedback and skills; Lambda stores in DynamoDB.
5. Lambda matches skills to jobs in DynamoDB and returns suggestions.
6. Frontend displays feedback, skill gaps, and job suggestions.

## Security
- HTTPS for all API and frontend communication.
- S3 server-side encryption.
- IAM roles with least privilege for Lambda.
- Cognito JWT tokens for authentication.

## AWS Free Tier Considerations
- Lambda: <1M requests/month.
- S3: <5GB storage, 20,000 GET, 2,000 PUT requests.
- DynamoDB: <25,000 read/write units.
- Cognito: <50,000 monthly active users.
- Amplify: <1,000 build minutes, 5GB hosting storage.