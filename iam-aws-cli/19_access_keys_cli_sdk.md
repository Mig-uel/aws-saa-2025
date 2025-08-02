# AWS Access Keys, CLI, and SDK

## How Can Users Access AWS Resources?

Users can access AWS resources through various methods, including:

- **AWS Management Console**: A web-based interface for managing AWS services.

  - Protected by password + Multi-Factor Authentication (MFA).

- **AWS Command Line Interface (CLI)**: A tool for managing AWS services using commands in your command-line shell.

  - Requires access keys (Access Key ID and Secret Access Key).
  - Can be configured to use MFA for additional security.

- **AWS SDKs**: Software Development Kits that allow developers to interact with AWS services using programming languages.
  - Also requires access keys.
  - Can be configured to use MFA.

We can generate access keys for users, which consist of an Access Key ID and a Secret Access Key, through the AWS Management Console. These keys are used to sign programmatic requests to AWS services.

Users manage their own access keys, and it is recommended to rotate them regularly for security purposes.

Access keys should be treated like passwords and kept secure. They should not be hard-coded in applications or shared publicly.

For comparison, Access Key ID is like a username, and Secret Access Key is like a password. Together, they authenticate the user to AWS services.

## What's the AWS CLI?

The AWS Command Line Interface (CLI) is a unified tool that provides a consistent interface for interacting with all parts of AWS. With the AWS CLI, you can control multiple AWS services from the command line and automate them through scripts.

- It is a tool that enables you to interact with AWS services using commands in your terminal or command prompt.
- It provides direct access to the public APIs of AWS services.
- It supports scripting and automation, allowing users to write scripts to automate tasks.
- It is open-source and can be installed on various operating systems, including Windows, macOS, and Linux.
- An alternative to using the AWS Management Console for managing AWS resources.

## What's the AWS SDK?

The AWS SDK (Software Development Kit) is a collection of libraries and tools that allow developers to interact with AWS services using programming languages. The SDKs provide a convenient way to access AWS services programmatically.

- The AWS SDK is a set of libraries that allow developers to interact with AWS services using programming languages such as Python, Java, JavaScript, Ruby, and more.
- Enables you to access and manage AWS services programmatically.
- You embed the SDK in your application code to make API calls to AWS services.
- Supports various platforms like mobile, web, IoT, and serverless applications.
- The AWS CLI is built on top of the AWS SDK for Python (Boto3), which means you can use the same SDK to build applications that interact with AWS services.
