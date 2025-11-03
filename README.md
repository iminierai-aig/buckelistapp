
# Bucket List App

A full-stack bucket list tracker application built with React and AWS Amplify, allowing users to create, manage, and track their bucket list items with image support.

<img width="1607" height="731" alt="image" src="https://github.com/user-attachments/assets/1ecb7824-3146-4ad7-9665-8cf7ae704fae" />

## Overview

This application provides a user-friendly interface for managing personal bucket list items with full authentication, cloud storage, and real-time data synchronization powered by AWS services.

## Features

- **User Authentication**: Secure login and signup functionality using AWS Amplify Authentication
- **Bucket List Management**: Create, read, update, and delete bucket list items
- **Image Upload**: Attach images to bucket list items stored in AWS S3
- **Real-time Sync**: Automatic data synchronization across devices
- **Responsive Design**: Mobile-friendly React interface
- **Cloud Backend**: Fully serverless architecture using AWS services

## Tech Stack

### Frontend
- **React**: JavaScript library for building the user interface
- **AWS Amplify SDK**: Integration with AWS backend services

### Backend & Infrastructure
- **AWS Amplify**: Deployment and hosting of frontend and backend services
- **AWS AppSync**: GraphQL API management and real-time data synchronization
- **GraphQL**: Query language for efficient data fetching
- **Amazon DynamoDB**: NoSQL database for storing bucket list items
- **Amazon S3**: Object storage for user-uploaded images
- **AWS Amplify Authentication**: User authentication and authorization

## Architecture

The application follows a serverless architecture pattern:

1. **Frontend**: React application hosted on AWS Amplify Hosting
2. **API Layer**: GraphQL API managed by AWS AppSync
3. **Data Layer**: DynamoDB tables for structured data storage
4. **Storage Layer**: S3 buckets for image file storage
5. **Authentication**: AWS Cognito user pools for secure authentication

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v14 or higher)
- npm or yarn
- AWS Account
- AWS Amplify CLI

```bash
npm install -g @aws-amplify/cli
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/iminierai-aig/buckelistapp.git
cd buckelistapp
```

2. Install dependencies:
```bash
npm install
```

3. Configure AWS Amplify:
```bash
amplify configure
```

4. Initialize Amplify in your project:
```bash
amplify init
```

5. Pull the backend environment:
```bash
amplify pull
```

## Configuration

### Setting up Authentication

Configure authentication using Amplify Studio or CLI:

```bash
amplify add auth
```

### Setting up the GraphQL API

The GraphQL schema defines the data model for bucket list items:

```bash
amplify add api
```

### Setting up Storage

Configure S3 storage for image uploads:

```bash
amplify add storage
```

## Deployment

### Deploy Backend

Push your backend configuration to AWS:

```bash
amplify push
```

### Deploy Frontend

The frontend is automatically deployed through AWS Amplify Hosting when you push to your connected GitHub repository.

Alternatively, you can manually deploy:

```bash
amplify publish
```

## Development

Run the application locally:

```bash
npm start
```

The application will open in your browser at `http://localhost:3000`.

## GraphQL Schema

The application uses a GraphQL schema to define the data structure for bucket list items. Key types include:

- **BucketListItem**: Main entity representing a bucket list item
- **User**: User information linked to authentication
- **Image**: Metadata for uploaded images

## Usage

1. **Sign Up/Login**: Create an account or log in with existing credentials
2. **Add Item**: Create a new bucket list item with a title, description, and optional image
3. **View Items**: Browse your bucket list in an organized view
4. **Update Item**: Edit existing items to track progress or add details
5. **Delete Item**: Remove completed or unwanted items
6. **Upload Images**: Attach images to visualize your bucket list goals

## Project Structure

```
buckelistapp/
├── src/
│   ├── components/      # React components
│   ├── graphql/         # GraphQL queries and mutations
│   ├── models/          # Data models
│   └── App.js           # Main application component
├── amplify/
│   ├── backend/         # Backend configuration
│   └── team-provider-info.json
├── public/              # Static files
└── package.json         # Project dependencies
```

## AWS Services Used

- **AWS Amplify**: Full-stack development platform
- **AWS AppSync**: Managed GraphQL service
- **Amazon DynamoDB**: NoSQL database service
- **Amazon S3**: Object storage service
- **Amazon Cognito**: User authentication service
- **AWS CloudFormation**: Infrastructure as code (managed by Amplify)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Security

- All user data is encrypted in transit and at rest
- Authentication is handled securely through AWS Cognito
- API access is controlled through AWS AppSync authorization rules
- Images are stored in private S3 buckets with proper access controls

## Troubleshooting

### Common Issues

**Issue**: Amplify CLI errors during setup
- **Solution**: Ensure you have the latest version of Amplify CLI installed

**Issue**: Authentication errors
- **Solution**: Verify your AWS Cognito user pool configuration

**Issue**: GraphQL API errors
- **Solution**: Check your AppSync API configuration and schema

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Built with AWS Amplify
- Powered by React
- GraphQL API managed by AWS AppSync
---

**Note**: Make sure to configure your AWS credentials and set up appropriate IAM roles before deploying this application.














