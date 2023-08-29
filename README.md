# AI Photo Album Web Application

This application is an intelligent photo album that allows users to search for images using natural language through both text and voice. Users can upload images and search for images by people, objects, actions, landmarks, and much more.

## Features:

- Natural Language Search through Text & Voice
- Powered by AWS Lex, OpenSearch, Rekognition, Lambda, and S3
- Auto-indexing of images when uploaded
- Ability to attach custom labels to photos
- Voice accessibility in frontend

## Implementation Outline:

1. **OpenSearch Setup**: Deployed an OpenSearch instance inside a VPC for secure and scalable searching.
2. **Image Upload & Indexing**: Upload images to an S3 bucket and trigger Lambda functions for indexing in OpenSearch.
3. **Natural Language Search**: Utilized Amazon Lex for search queries and fetch results from OpenSearch.
4. **API Layer**: Implement API Gateway for two main functionalities - uploading photos and searching.
5. **Frontend**: A user-friendly frontend for search and upload. Can also specify custom labels during upload.
6. **Voice Accessibility**: Frontend implementation to allow voice-based searches using Amazon Transcribe.
7. **Continuous Deployment**: Used AWS CodePipeline for seamless CI/CD of the application.
8. **Infrastructure as Code**: Used AWS CloudFormation for replicable and managed infrastructure deployment.

## Getting Started:

### Prerequisites:

1. AWS Account
2. Node.js and npm for frontend
3. Basic knowledge of AWS services listed in the outline

### Deployment:

1. **AWS CloudFormation**:
   - Use the provided CloudFormation template (T1) to stand up the entire stack for the application.
   - The template includes all necessary resources and permissions.

2. **Continuous Deployment**:
   - Push your updates to the GitHub repository.
   - AWS CodePipeline will automatically pick changes and deploy them.

## User Guide:

1. **Visit the S3 Hosted URL**:
   - Access the photo album application.
   
2. **Search Photos**:
   - Use natural language (text or voice) to search for photos.
   - View relevant results based on the search query.
   
3. **Upload Photos**:
   - Add new photos to the album.
   - Optionally, attach custom labels during upload.
   - Newly uploaded photos will be available in search results.

## Helpful Resources:

- [OpenSearch Getting Started](https://www.elastic.co/webinars/getting-started-OpenSearch?elektra=home&storm=sub1)
- [API Gateway S3 Proxy Setup](https://docs.aws.amazon.com/apigateway/latest/developerguide/integrating-api-with-aws-services-s3.html)
- [AWS Rekognition](https://aws.amazon.com/rekognition/)
- [AWS Transcribe](https://aws.amazon.com/transcribe/)
- [AWS CloudFormation](https://aws.amazon.com/cloudformation/)
- [Swagger API documentation](https://github.com/001000001/ai-photo-search-columbia-f2018/blob/master/swagger.yaml)

