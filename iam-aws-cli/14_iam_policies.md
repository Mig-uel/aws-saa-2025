# IAM Policies

## IAM Policies Inheritance

Let's imagine we have a group of `Developers` and we apply a policy to this group that allows them to perform actions on S3 buckets. The policy will be inherited by all users in the `Developers` group.

Now, we also have another group called `Operations` that has a policy allowing them to perform actions on EC2 instances. If a user is part of both groups, they will inherit permissions from both policies.

This means that the user will be able to perform actions on both S3 buckets and EC2 instances, as long as the actions are allowed by the policies attached to their groups.

Additionally, if a user is directly assigned an inline policy that allows them to perform actions on DynamoDB, they will also have those permissions in addition to the permissions inherited from their groups.

## IAM Policies Structure

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "ExampleStatement",
      "Effect": "Allow",
      "Action": ["s3:ListBucket", "s3:GetObject"],
      "Resource": [
        "arn:aws:s3:::example-bucket",
        "arn:aws:s3:::example-bucket/*"
      ],
      "Condition": {
        "StringEquals": {
          "aws:username": "exampleUser"
        }
      }
    }
  ]
}
```

At a high level, an IAM policy consists of the following components:

- **Version**: Specifies the version of the policy language. The current version is `2012-10-17`.
- **Id**: An optional identifier for the policy.
- **Statement**: An array of statements that define the permissions. Each statement can include:
  - **Sid**: An optional identifier for the statement.
  - **Effect**: Specifies whether the statement allows or denies access. Possible values are `Allow` or `Deny`.
  - **Action**: Specifies the actions that are allowed or denied. This can be a single action or a list of actions.
  - **Resource**: Specifies the AWS resources to which the actions apply. This can be a specific resource ARN or a wildcard (`*`) to apply to all resources.
  - **Condition**: (Optional) Specifies conditions under which the policy is in effect. Conditions can be based on various factors such as IP address, time of day, or request parameters.
- **Principal**: (Optional) Specifies the user, account, service, or other entity that is allowed or denied access.
