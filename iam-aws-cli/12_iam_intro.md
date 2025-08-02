# IAM (Identity and Access Management) Introduction: Users, Groups, and Policies

## What is IAM?

IAM stands for Identity and Access Management and is a Global AWS service.

IAM (Identity and Access Management) is a web service that helps you securely control access to AWS resources. It allows you to manage users, groups, roles, and permissions to ensure that only authorized users can access specific AWS services and resources.

- Root account is created by default when you create an AWS account and should not be used for day-to-day tasks or shared with others.

With your root account, you should create users that have the permissions they need to perform their tasks. You can create users, groups, and roles, and assign permissions to them using policies.

- Users are individual accounts that can be created for people or applications that need access to AWS resources.
- Groups are collections of users that can be managed together, allowing you to assign permissions to multiple users at once.
  - Groups can only contain users, not other groups or roles.
  - Some users do not need to belong to a group, and you can assign permissions directly to them (not recommended).
  - A user can belong to multiple groups, and the permissions from all groups are aggregated.
- Policies are documents that define permissions and can be attached to users, groups, or roles. They specify what actions are allowed or denied on specific AWS resources.

## IAM: Permissions and Policies

An IAM policy is a JSON document that specifies who can do what in your AWS organization. It defines permissions for users, groups, or roles.

- Users or groups can be assigned JSON documents called IAM policies that define their permissions.

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "*"
    }
  ]
}
```

- The above policy allows the user to list all S3 buckets in the account.
- **Effect** specifies whether the action is allowed or denied.
- **Action** specifies the specific AWS service and action that is allowed or denied.
- **Resource** specifies the AWS resource to which the policy applies.

In AWS, you don't allow everyone to do everything. Instead, you start with a policy that denies all actions and then add specific permissions for users, groups, or roles as needed.

This is known as the least privilege principle, which means giving users only the permissions they need to perform their tasks and nothing more.
