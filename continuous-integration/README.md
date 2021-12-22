
# Define and implement [continuous integration](continuous-integration/README.md) (20-25%)
## Design build automation
- integrate the build pipeline with external tools (e.g., Dependency and security scanning, Code coverage)
- implement quality gates (e.g., code coverage, internationalization, peer review)
- design a testing strategy (e.g., integration, load, fuzz, API, chaos)
- integrate multiple tools (e.g., GitHub Actions, Azure Pipeline, Jenkins)
## Design a package management strategy
- recommend package management tools (e.g. GitHub Packages, Azure Artifacts, Azure
## Automation Runbooks Gallery, Nuget, Jfrog, Artifactory)
- design an Azure Artifacts implementation including linked feeds
- design versioning strategy for code assets (e.g., SemVer, date based)
- plan for assessing and updating and reporting package dependencies (GitHub
## Automated Security Updates, NuKeeper, GreenKeeper)
- design a versioning strategy for packages (e.g., SemVer, date based)
- design a versioning strategy for deployment artifacts
## Design an application infrastructure management strategy
- assess a configuration management mechanism for application infrastructure
- define and enforce desired state configuration for environments
## Implement a build strategy
- design and implement build agent infrastructure (include cost, tool selection, licenses, maintainability)
- develop and implement build trigger rules
- develop build pipelines
- design build orchestration (products that are composed of multiple builds)
- integrate configuration into build process
- develop complex build scenarios (e.g., containerized agents, hybrid, GPU)
## Maintain build strategy
- monitor pipeline health (failure rate, duration, flaky tests)
- optimize build (cost, time, performance, reliability)
- analyze CI load to determine build agent configuration and capacity
## Design a process for standardizing builds across organization
- manage self-hosted build agents (VM templates, containerization, etc.)
- create reuseable build subsystems ([YAML templates](https://docs.microsoft.com/en-us/azure/devops/pipelines/yaml-schema?view=azure-devops&tabs=schema%2Cparameter-schema), [Task Groups](https://docs.microsoft.com/en-us/azure/devops/pipelines/library/task-groups?view=azure-devops), [Variable Groups](https://docs.microsoft.com/en-us/azure/devops/pipelines/library/variable-groups?view=azure-devops&tabs=yaml))
__________________________________________________________________________________________



# Continuous Integration (CI)

The practice of automating the integration of code changes from multiple contributors into a single software project. It's a primary DevOps best practice, allowing developers to frequently merge code changes into a central repository where builds and tests then run.

- Integrating code frequently does not guarante the quality of the code or functionality
- Manual processes can be used to ensure standards, however is costly and slow
- The level of integration must be balanced the QA measures
- CI relies on test suites and automation to run against the the new build
- If build or test fails the dev team must fix the build
- The goal of CI is a simple repeatable process that is part of the day-to-day of the dev team

## The Four Pillars
1. **Version control** to manage source code; [Git](https://git-scm.com/),  [Apache Subversion](https://subversion.apache.org/), [Team Foundation Version Control](https://docs.microsoft.com/en-us/azure/devops/repos/tfvc/what-is-tfvc?view=azure-devops&viewFallbackFrom=vsts)

2. **Package management** to install, uninstall, and manage software packages; [NuGet](https://www.nuget.org/), [Node Package Manager (NPM)](https://www.npmjs.com/), [Chocolatey](https://chocolatey.org/), [HomeBrew](https://brew.sh/), [RPM](http://rpm.org/)
   
3. **Continuous integration** merges all developer working copies to a shared mainline several times a day; [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/), [TeamCity](https://www.jetbrains.com/teamcity/), [Jenkins](https://www.jenkins.io/)

4. **Automated build** creates a software build including compiling, packaging, and running automated tests; [Apache Ant](https://ant.apache.org/), [NAnt](http://nant.sourceforge.net/), [Gradle](https://gradle.org/)

## Benefits of CI
- Improving code quality based on rapid feedback
- Triggering automated testing for every code change
- Reducing build times for rapid feedback and early detection of problems (risk reduction)
- Better managing technical debt and conducting code analysis
- Reducing long, difficult, and bug-inducing merges
- Increasing confidence in codebase health long before production deployment
