<p align="left">
  <img src="Role.png" width="50" height="50">

# [IAM ROLE](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/iam.html?highlight=role#IAM.Role)

- Roles have associated permissions that allow or deny specific actions
- These roles can be assumed for `temporary amounts of time` 
- They are intended to be used not by physical people, but instead that will be used by AWS services 
- IAM roles are ideal for situations in which access to services or resources needs to be granted temporarily, instead of long-term
- Almost all services in AWS can use roles, but a very common use case to create a role are EC2 instances and lambda functions
