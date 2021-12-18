# Continuous Integration

Continuous integration (CI) is the practice of automating the integration of code changes from multiple contributors into a single software project. It's a primary DevOps best practice, allowing developers to frequently merge code changes into a central repository where builds and tests then run.

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
