# IAM Best Practices

## IAM Guidelines & Best Practices

1. **Use IAM Users and Groups**:

- Create individual IAM users for each person who needs access to your AWS account.
- Use IAM groups to manage permissions for multiple users at once.
- Do not use the root account for everyday tasks. Create an IAM user with administrative privileges instead.
- One physical user = one AWS IAM user. Do not share accounts.
- Create a strong password policy for IAM users.

2. **Enforce Multi-Factor Authentication (MFA)**:

- Enable MFA for all IAM users, especially those with administrative privileges.
- Use hardware or virtual MFA devices for added security.

3. **Use IAM Roles**:

- Use IAM roles for applications that run on Amazon EC2 instances, AWS Lambda functions, or other AWS services.
- Use roles to delegate access to users or services without sharing long-term credentials.

4. **Implement the Principle of Least Privilege**:

- Grant only the permissions necessary for users to perform their tasks.
- Regularly review and refine permissions to ensure they are still appropriate.

5. **Audit and Monitor IAM Activity**:

- Enable AWS CloudTrail to log all API calls made in your account.
- Use AWS Config to monitor changes to IAM resources.
- Regularly review IAM policies and permissions using the IAM Access Analyzer.
