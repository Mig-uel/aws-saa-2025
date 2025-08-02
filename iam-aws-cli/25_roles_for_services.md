# IAM Roles for AWS Services

## IAM Roles for Services

AWS services can assume IAM roles to perform actions on your behalf. This is particularly useful for granting permissions to services without needing to manage access keys.

- We assign permissions to AWS services using IAM roles.
- These IAM roles will be just like a user, but they are intended be used not by a human, but by a service.

For example, an EC2 instance may want to perform some actions on AWS. To do so, we need to give permission to our EC2 instance to perform those actions. We can do this by creating an IAM role and assigning it to the EC2 instance.

Some common roles for AWS services include:

- **EC2 Instance Role**: Allows EC2 instances to access other AWS services.
- **Lambda Execution Role**: Grants AWS Lambda functions permission to access other AWS services.
- **ECS Task Role**: Allows Amazon ECS tasks to access AWS services.
- **S3 Access Role**: Grants access to Amazon S3 buckets.
