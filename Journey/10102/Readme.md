<p align="left">
  <img src="IAM.png" width="50" height="50">
  <img src="Permissions.png" width="50" height="50">
  <img src="LongTermSecCred.png" width="50" height="50"></p>

# [IAM](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/iam.html#user)

- `One user` represents `one person` in your organization
- Users can be grouped
- Users don't have to belong to a group
- One user can belong to multiple groups
- Groups can only contain users, not other groups
- When you create an IAM user, by default, it has no permissions
- You have to explicitly give the user permission to do anything in that account
- The way that you grant or deny permission is to associate what is called an `IAM policy` to an IAM user
- You can attach a policy to a group and all of the users in that group will have those permissions
