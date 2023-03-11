# AWS

## IAM

### IAM: Users & Groups

Users and Groups are created so that users can run specific services only not all which can cause cost.
Also provides security.

- IAM = Identity and Access Management, Global service
- Root account created by default, shouldn’t be used or shared - Root is a God Mode in AWS.
- Users are people within your organization, and can be grouped
- Groups only contain users, not other groups
- Users don’t have to belong to a group, and user can belong to multiple groups
 
  ![image](https://user-images.githubusercontent.com/73632896/223759721-b2a7f127-c7a6-41f4-b4bc-79513c5ffeb0.png)
  
### IAM: Permissions
  
- Users or Groups can be assigned JSON documents called policies.
- These policies define the permissions of the users.
- In AWS you apply the least privilege principle: don’t give more permissions than a user needs.
- e.g.
  
  ![image](https://user-images.githubusercontent.com/73632896/223760365-2ea49bce-f6d9-41c4-b953-6d6e05ee2618.png)

### IAM Policies:

IAM Policies are used to give permission to Users/Groups.

![image](https://user-images.githubusercontent.com/73632896/223773309-cd628376-0901-47de-9de2-1f2c05ea16f5.png)

 #### IAM Policies Structure
 
 - **Consists of**
   - **Version:** policy language version, always include “2012-10-17”
   - **Id:** an identifier for the policy (optional)
   - **Statement:** one or more individual statements (required)
 - **Statements consists of**
   - **Sid:** an identifier for the statement (optional)
   - **Effect:** whether the statement allows or denies access (Allow, Deny)
   - **Principal:** account/user/role to which this policy applied to
   - **Action:** list of actions this policy allows or denies
   - **Resource:** list of resources to which the actions applied to
   - **Condition:** conditions for when this policy is in effect (optional)

   ![image](https://user-images.githubusercontent.com/73632896/223774251-72bf19b1-5e9c-456a-94df-fce5f33fe3fc.png)
   
  #### IAM – Password Policy

  Strong passwords = higher security for your account
  - In AWS, you can setup a password policy:
    - Set a minimum password length
    - Require specific character types:
      - including uppercase letters
      - lowercase letters
      - numbers
      - non-alphanumeric characters
    - Allow all IAM users to change their own passwords
    - Require users to change their password after some time (password expiration)
    - Prevent password re-use

  #### Multi Factor Authentication - MFA
  
  - Users have access to your account and can possibly change configurations or delete resources in your AWS account
  - You want to protect your Root Accounts and IAM users
  - MFA = password you know + security device you own
      ![image](https://user-images.githubusercontent.com/73632896/223782033-b0dd13c7-9a88-4a12-81e2-60edbf9861e3.png)
  - Main benefit of MFA: if a password is stolen or hacked, the account is not compromised
 
  #### MFA devices options in AWS
  
  1. **Virtual MFA Device** - Support for multiple tokens on a single device.


     ![image](https://user-images.githubusercontent.com/73632896/223782742-64a49448-f4b7-404b-b771-139f9a1abdb0.png)

  2. **Universal 2nd Factor (U2F) Security Key** - Support for multiple root and IAM users using a single security key


     ![image](https://user-images.githubusercontent.com/73632896/223782917-e4c51b2e-aa87-4679-b98d-b43736745985.png)

  3. **Hardware Key Fob MFA Device**


     ![image](https://user-images.githubusercontent.com/73632896/223783032-1ea5c33f-0eda-4a2b-967b-6d919ae8207d.png)

  4. **Hardware Key Fob MFA Device for AWS GovCloud (US)**


     ![image](https://user-images.githubusercontent.com/73632896/223783115-b42ff5b2-ed0a-48f9-9e92-ff7ff297af21.png)
     
     
### How can users access AWS ?

- To access AWS, you have three options:
  - AWS Management Console (protected by password + MFA)
  - AWS Command Line Interface (CLI): protected by access keys
  - AWS Software Developer Kit (SDK) - for code: protected by access keys
- Access Keys are generated through the AWS Console
- Users manage their own access keys
- Access Keys are secret, just like a password. Don’t share them
- Access Key ID ~= username
- Secret Access Key ~= password

  #### Example (Fake) Access Keys
  
  ![image](https://user-images.githubusercontent.com/73632896/224468974-84771a83-b61f-44cb-b9f6-ac5d710945bf.png)
  
  - Access key ID: AKIASK4E37PV4983d6C
  - Secret Access Key: AZPN3zojWozWCndIjhB0Unh8239a1bzbzO5fqqkZq
  - Remember: don’t share your access keys

  #### What’s the AWS CLI?
  
  - A tool that enables you to interact with AWS services using commands in your command-line shell
  - Direct access to the public APIs of AWS services
  - You can develop scripts to manage your resources
  - It’s open-source [(https://aws.amazon.com/cli/)](https://aws.amazon.com/cli/)
  - Alternative to using AWS Management Console

  ![image](https://user-images.githubusercontent.com/73632896/224469061-21027dc9-5da7-401e-80ca-771055c7bb96.png)
  
    ##### AWS CLI
    
    1. **create access key for command line interface.**
    2. **configure aws-cli**

      C:\Users\shreenath>aws configure
      AWS Access Key ID [None]: <Access Key ID>
      AWS Secret Access Key [None]: <Secret Access Key>
      Default region name [None]: ap-south-1
      Default output format [None]:

    3. **get IAM users list.**

      C:\Users\shreenath>aws iam list-users
      {
          "Users": [
              {
                  "Path": "/",
                  "UserName": "shreenath",
                  "UserId": "<User ID>",
                  "Arn": "arn:aws:iam::<Account ID>:user/shreenath",
                  "CreateDate": "2023-03-08T16:01:48+00:00",
                  "PasswordLastUsed": "2023-03-11T06:53:57+00:00"
              }
          ]
       }
       
     4. **In case of no permission for list-users operation**
     ```
     C:\Users\shreenath>aws iam list-users

     An error occurred (AccessDenied) when calling the ListUsers operation: User: arn:aws:iam::<Account ID>:user/shreenath is not authorized to perform: iam:ListUsers      on resource: arn:aws:iam::<Account ID>:user/ because no identity-based policy allows the iam:ListUsers action
     ```
 
  #### What’s the AWS SDK?
  
  - AWS Software Development Kit (AWS SDK)
  - Language-specific APIs (set of libraries)
  - Enables you to access and manage AWS services programmatically
  - Embedded within your application
  - Supports
    - SDKs (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
    - Mobile SDKs (Android, iOS, …)
    - IoT Device SDKs (Embedded C, Arduino, …)
  - Example: AWS CLI is built on AWS SDK for Python

  ![image](https://user-images.githubusercontent.com/73632896/224469179-9e53cd02-2c3f-476e-bca3-9e6810d2b199.png)


