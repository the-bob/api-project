## Change Management/Versioning/Migration



## SCM

We'll go with [GIT](https://git-scm.com) for our SCM, 


## Versioning.

We'll go with [semver](https://semver.org) and [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) to follow a more standard approach, this will enable us to automatically Generate our CHANGELOG files via [commitizen](https://commitizen-tools.github.io/commitizen/), to further simplify version management of the tool/software we'll go with [trunk based development](https://trunkbaseddevelopment.com) and it will be then incremented based of `main` from it's commits from the short lived branches through conventional commits and it will be incremented by semver.

**NOTE:** The chosen CI system (GitHub Actions) have a lot of OOTB Actions to support the tools and best practices above. 

<hr/>

[back](./README.md)
