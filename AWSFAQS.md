
# FAQS
- [Security and Identity](#seciden)
    - [Identity and Access Management](#iam)
- [What is DevOps](#devops)
- [Path](#path)
- [TODO](#todo)


## Security and Identity <a name = "seciden"></a>

### Identity and Access Management <a name = "iam"></a>

- Any AWS customer can use IAM. The service is offered at **no additional charge**. You will be *charged only for the use of other AWS services by your users*.

 -------------
- A **user** is a unique identity recognized by AWS services and applications. A user can be an individual, system, or application requiring access to AWS services.
    - IAM user
    - Federated user ( users managed outside of AWS in your corporate directory )
- Explicit permissions govern a user's ability to call AWS services. *By default, users have no ability to call service APIs on behalf of the account.*
-  Users are **global entities**.Users can use AWS services in any geographic region.
- Can I set usage quotas on IAM users? No. 
- IAM users credentials:
  - AWS access key
  - X.509 certificate
  - SSH key (Currently, IAM users can use their SSH keys only with AWS CodeCommit to access their repositories.)
  - password for web app logins
  - an MFA device. 

 -------------
- A **group** is a collection of IAM users. 
    - A user can belong to multiple groups.
    - *Groups cannot belong to other groups.*
  - Groups *do not have security credentials*, and cannot access web services directly; they exist solely to make it easier to manage user permissions.


 -------------
- An IAM **role** is an IAM entity that defines a set of permissions for making AWS service requests. Not associated with a specific user or group. 
  -  Trusted entities assume roles, such as IAM users, applications, or AWS services such as EC2.
  -  You assume an IAM role by calling the AWS Security Token Service (STS) AssumeRole APIs (in other words, AssumeRole, AssumeRoleWithWebIdentity, and AssumeRoleWithSAML). 
  -  **no limit to the number of IAM roles** you can assume, but you can only act as one IAM role when making requests to AWS services.
  -  **free of charge**

