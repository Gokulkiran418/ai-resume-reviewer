# AI Resume Reviewer & Job Matcher(Ongoing Project)

A web app for resume analysis and job matching using AWS and GPT-4o.

## Technology Stack
- **Frontend**: Next.js (TypeScript, Tailwind CSS), AWS Amplify
- **Backend**: AWS Lambda (Python 3.12), API Gateway
- **Storage**: Amazon S3
- **Database**: Amazon DynamoDB
- **Authentication**: Amazon Cognito
- **AI**: OpenAI GPT-4o API
- **Libraries**: PyPDF2, Boto3, OpenAI Python SDK

## Setup
1. **Frontend**:
   - `cd frontend && npm install`
   - Install AWS Amplify: `npm install @aws-amplify/auth @aws-amplify/ui-react`
2. **Backend**:
   - `cd backend && python3 -m venv venv && source venv/bin/activate`
   - Install dependencies: `pip install boto3 PyPDF2 openai`
3. Install AWS CLI: `pip install awscli`
4. Get OpenAI API key from [OpenAI](https://platform.openai.com).

## Next Steps
- Configure AWS services (Step 4).
- Develop frontend and backend (Steps 5-7).