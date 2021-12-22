
# What is Source Control

- Allows developers to collaborate on code and track changes. 
- Provide a running history of code development
- CI and DevOps rely on source control 
- Tracks every change to the software (who, what, when)
- Allows roll back to previously working versions
- a enabler for daily work

## Authentication strategies

The **GitHub** authentication strategy authenticates users using a GitHub account and OAuth 2.0 tokens. The strategy requires a verify callback, which accepts these credentials and calls done providing a user, as well as options specifying a client ID, client secret, and callback URL.
  
Azure DevOps has the following key concepts:
- Users are typically added to one or more security groups
- Security groups are assigned [permissions](https://docs.microsoft.com/en-us/azure/devops/organizations/security/permissions-lookup-guide?view=azure-devops) which either allow or deny access to a feature 
- Members of the security group inherit the permissions assigned to the group
- Each user is also assigned an access level which grants or restricts access to select web portal features
- Permissions are set at various levels for most objects, such as repositories, pipelines, area paths, and so on.
- Other permissions are managed through role-based assignments, such as team administrator role, extension management role, and various pipeline resource roles.
- As new features are introduced you may need to enable their feature flag to access them.