
## Manage source control (10-15%)
### Develop a modern source control strategy
- integrate/migrate disparate source control systems (e.g., GitHub, Azure Repos)
- design authentication strategies
- design approach for managing large binary files (e.g., Git LFS)
- design approach for cross repository sharing (e.g., Git sub-modules, packages)
- implement workflow hooks
- design approach for efficient code reviews (e.g., GitHub code review assignments, schedule reminders, Pull Analytics)
### Plan and implement branching strategies for the source code
- define Pull Requests (PR) guidelines to enforce work item correlation
- implement branch merging restrictions (e.g., branch policies, branch protections, manual, etc.)
- define branch strategy (e.g., trunk based, feature branch, release branch, GitHub flow)
- design and implement a PR workflow (code reviews, approvals)
- enforce static code analysis for code-quality consistency on PR
### Configure repositories
- configure permissions in the source control repository
- organize the repository with git-tags
- plan for handling oversized repositories
- plan for content recovery in all repository states
- purge data from source control
### Integrate source control with tools
- integrate GitHub with DevOps pipelines
- integrate GitHub with identity management solutions (Azure AD)
- design for GitOps
- design for ChatOps
- integrate source control artifacts for human consumption (e.g., Git changelog)
- integrate GitHub Codespaces



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