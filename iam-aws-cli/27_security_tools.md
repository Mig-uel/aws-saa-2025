# IAM Security Tools

## IAM Credential Report (account-level)

The IAM Credential Report provides a detailed report of all IAM users in your AWS account, including their access keys, password status, and MFA (Multi-Factor Authentication) status. This report is essential for auditing and ensuring that your IAM users follow security best practices.

- This report lists all your account's IAM users and the status of their various credentials.
- It includes information such as:

  - User names
  - Access key IDs
  - Access key status (Active/Inactive)
  - Password last used date
  - MFA device status

## IAM Access Advisor (user-level)

The IAM Access Advisor provides insights into the permissions granted to IAM users and roles, helping you understand which permissions are actually being used. This tool is crucial for identifying unused permissions and reducing the risk of over-privileged accounts.

- It shows the last accessed date for each service that a user or role has permissions to access.
- This information helps you determine whether to keep, modify, or remove permissions based on actual usage.
- You can use this tool to:
  - Identify unused permissions
  - Reduce the risk of over-privileged accounts
  - Improve security posture by following the principle of least privilege
