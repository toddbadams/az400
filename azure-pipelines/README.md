
# Azure Pipelines
- automatically build and valide every pull request (PR)
- works with just about any language, including [Python](https://www.python.org/), [Java](https://www.java.com/en/), [JavaScript](https://www.javascript.com/), [PHP](https://www.php.net/), [Ruby](https://www.ruby-lang.org/en/), [C#](https://docs.microsoft.com/en-us/dotnet/csharp/), [C++](https://en.wikipedia.org/wiki/C%2B%2B), and [Go](https://go.dev/)
- combines continuous integration (CI) with continuous delivery (CD)
- Works with [Azure Repos](https://azure.microsoft.com/en-us/services/devops/repos/) and [GitHub](https://github.com/), 

| Repository type          | Azure Pipelines (YAML) | Azure Pipelines (classic editor) |
|--------------------------|------------------------|----------------------------------|
| Azure Repos Git          | Yes                    | Yes                              |
| Azure Repos TFVC         | No                     | Yes                              |
| Bitbucket Cloud          | Yes                    | Yes                              |
| Other Git (generic)      | No                     | Yes                              |
| GitHub                   | Yes                    | Yes                              |
| GitHub Enterprise Server | Yes                    | Yes                              |
| Subversion               | No                     | Yes                              |

## Recommened Content
- [Create your first pipline](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=net%2Ctfs-2018-2%2Cbrowser) - step-by-step guide to using Azure Pipelines to build a sample application
- [Use Azure Pipelines](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops) - learn the basics
- [DevOps Starter](https://docs.microsoft.com/en-us/azure/devops-project/overview) - understand the value of DevOps Starter

## Overview

![Key Concepts](key-concepts-overview.svg)

- A [trigger](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#trigger) tells a Pipeline to run.
- A [pipeline](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#pipeline) is made up of one or more stages. A pipeline can deploy to one or more [environments](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#environment).
- A [stage](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#stage) is a way of organizing jobs in a pipeline and each stage can have one or more jobs.
- Each [job](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#job) runs on one agent. A job can also be agentless.
- Each [agent](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#agent) runs a job that contains one or more steps.
- A [step](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#step) can be a task or script and is the smallest building block of a pipeline.
- A [task](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#task) is a pre-packaged script that performs an action, such as invoking a REST API or publishing a build artifact.
- An [artifact](https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/key-pipelines-concepts?view=azure-devops#artifact) is a collection of files or packages published by a run.


## YAML 

The pipeline is defined in  `azure-pipelines.yml` in the code repository

 ![Pipelines YAML intro image](pipelines-image-yaml.png)

- The pipeline is versioned with your code. 
- It follows the same branching structure. 
- You get validation of your changes through code reviews in pull requests and branch build policies.
- Every branch you use can modify the pipeline by modifying the azure-pipelines.yml file. 
- A change to the build process might cause a break or result in an unexpected outcome. Because the change is in version control with the rest of your codebase, you can more easily identify the issue.
- Certain pipeline [features]((https://docs.microsoft.com/en-us/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops#feature-availability) are only avialable using YAML