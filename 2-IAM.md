# AWS

## IAM

### IAM: Users & Groups

Users and Groups are created so that users can run specific services only not all which can cause cost.
Also provides security.

- IAM = Identity and Access Management, Global service
- Root account created by default, shouldn’t be used or shared
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
