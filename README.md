# AWS BedRock Text Summarization Project

## Overview

This project focuses on leveraging AWS BedRock, a fully managed service, for text summarization using the Coher foundation model. The objective is to improve productivity by providing summarized information for faster issue resolution, particularly in scenarios where technicians need quick insights into detailed issue logs.

## AWS Services Used

- **AWS BedRock**: Fully managed service for building and scaling generative AI applications with Foundational Models.
- **Lambda**: Serverless compute service used for executing the text summarization function.
- **API Gateway**: Facilitates the creation, deployment, and management of APIs, serving as the entry point for user requests.

## Workflow

1. **User Invocation**: User sends a REST API request along with a detailed issue log prompt.
2. **Lambda Function Trigger**: API Gateway triggers a Lambda function upon receiving the REST API request.
3. **Text Summarization**: Lambda function extracts the prompt, invokes the Coher foundation model through AWS BedRock, and processes the response.
4. **API Gateway Response**: Summarized text is returned via the HTTP response (status code: 200) through API Gateway.

## Implementation Steps

### Enable BedRock Models

- Access AWS account settings and enable BedRock models.

### Lambda Function Development

1. **Python-based Lambda Function**
    - Develop a Lambda function using Boto3 for AWS BedRock integration.
    - Ensure compatibility with the Coher model for text summarization.

2. **Boto3 Integration**
    - Initialize Boto3 client for AWS BedRock runtime.
    - Extract user prompt from the event.

3. **Invoke Coher Model**
    - Invoke Coher foundation model for text summarization.

4. **Processing and Response**
    - Process and return the summarized text in the HTTP response (status code: 200).

### API Gateway Creation

1. **REST API Setup**
    - Create a new REST API.

2. **Resource Configuration**
    - Configure resources and create a GET method for handling prompts.

### Testing and Deployment

1. **Initial Testing**
    - Test the Lambda function with hardcoded prompts.

2. **Dynamic Testing**
    - Progress to dynamic prompts and test the API through API Gateway.

3. **Deployment**
    - Deploy the API to a public stage for practical use.

### Additional Considerations

- Ensure Boto3 version is 1.28.63 or higher.
- Implement proper error handling in the Lambda function.
- Address security considerations in both Lambda function and API Gateway configurations.

## Significance

This project showcases the efficiency of AWS services, emphasizing the potential of text summarization for enhanced productivity in diverse industries. The integration of AWS BedRock's Coher model empowers technicians to make informed decisions swiftly, revolutionizing issue resolution in remote environments. The project's code and documentation can be found in this repository for reference and collaboration.
