# IAM MFA

We have two defense mechanisms in AWS IAM:

1. **Multi-Factor Authentication (MFA)**: This adds an extra layer of security by requiring users to provide two or more verification factors to gain access to AWS resources. This can include something they know (password) and something they have (a mobile device or hardware token).
2. **Password Policy**: This allows you to enforce specific requirements for user passwords, such as length, complexity, and expiration.

## IAM - Password Policy

IAM allows you to enforce a password policy for your users, which can include requirements such as minimum password length, complexity, and expiration. This helps ensure that user accounts are secure and that passwords are not easily guessable.

We define password policies to:

- Create strong passwords
  - Stronger passwords = higher security
- Set a minimum password length
- Require specific character types (uppercase, lowercase, numbers, symbols)
- Allow or disallow users to change their own passwords
- Set password expiration periods
- Prevent password reuse

A password policy is really helpful against brute-force attacks on your account but there is a better way to secure your account, which is by using Multi-Factor Authentication (MFA).

## IAM - Multi-Factor Authentication (MFA)

MFA is a security feature that requires users to provide two or more verification factors to gain access to AWS resources. This adds an extra layer of security beyond just a username and password.

MFA can be set up for the root user and for IAM users. It is highly recommended to enable MFA for all users, especially for the root user, to enhance security.

Why should you use MFA?

- Users have access to your AWS account and resources and can possibly change configurations, delete resources, or incur costs.

Because of this, you absolutely want to protect your root account and any IAM users with MFA.

MFA is a combination of something you know (your password) and something you have (a device that generates a time-based one-time password, or TOTP).
MFA devices can be either virtual (like an app on your smartphone) or hardware devices (like a physical token).

These two things together make it much harder for an attacker to gain access to your account, even if they have your password.

The main benefits of using MFA are:

- **Enhanced Security**: MFA adds an additional layer of security, making it much harder for unauthorized users to access your AWS account.
- **Protection Against Compromised Credentials**: Even if an attacker obtains your password, they would still need the second factor (MFA device) to gain access.
- **Compliance**: Many compliance frameworks require the use of MFA for sensitive accounts and operations, making it a best practice in cloud security.

## MFA Devices Options in AWS

AWS supports several types of MFA devices:

- **Virtual MFA Devices**: These are software-based applications that run on your smartphone or computer. Examples include Google Authenticator, Authy, and AWS's own Virtual MFA app.
- **Hardware MFA Devices**: These are physical devices that generate a time-based one-time password (TOTP). AWS provides hardware tokens that can be used for MFA.
- **U2F Security Key**: These are physical devices that support the Universal 2nd Factor (U2F) standard, such as YubiKey. They can be used for MFA in AWS.
- **SMS MFA**: This method sends a one-time password to your mobile phone via SMS. While convenient, it is less secure than other methods due to potential vulnerabilities in SMS delivery.

When setting up MFA, you can choose the type of device that best fits your needs and security requirements. Virtual MFA devices are often the most convenient, while hardware tokens provide a higher level of security.
