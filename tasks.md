## Task

[back](./README.md)

<hr/> 

a. how to start this project:

*NOTE:* On setting up the Repository Ideally through `IaC` for consistency such as `terraform` github provider.

- Setup the Repository for this Project via `GitHub`.
  - This includes setting up of the initial project structure, this can be done through `blitz.js` or other similar tools.
  - The project should also include the relevant automation scripts and `Dockerfile`
  - Setup `helm` template for the service.
  - Setup `devspace` or `tilt` for the service.
- Setup the Repository for the Infrastructure and leverage `CDK`'s Starter setup
- Setup the `CI` for both project 
  - There are reusable Official `GitHub Actions` for 
    - `Node` 
    - Static Code analysis (No specific Tool - see assumptions)
    - `commitizen` (for `conventional commits` and `semver`)
    - `Docker`
- NOTE: on the `CI` we can make the workflows reusable (`GitHub Actions Workflows`) (This will make it easier to start a new TypeScript project in the future).
  

- Develop the API Service (Or at least the minimal working Version) locally using `devspace` or `tilt` and deployed to a local `Kubernetes` Cluster (This can be using `minikube`, `k3s`, `rancher destop` etc)
  - In Emulating the `RDS MySQL` Server, we can use `localstack` and deployed against the local `k8s` server  
- Develop and Deploy (Ideally through `CD` via `GitHub Actions`) the minimal Viable Development Environment, then later the Higher Environment (Prod/Staging).
  - Leverage `EKS Blueprint` for the EKS Server (This will contain all the needed addons etc).
 

b. how this api should be built:
- The API Service Should be dockerized through `CI` via `GitHub Actions` (This should also cover other artifacts that the project may need to produce such as libs, docker images, docs etc.).
- Before the Build Dockerizes it, it needs to:
  - lint
  - test
  - static code analysis and security scanning  
  - build
  - (main branch) it will invoke `commitizen` to generate the needed CHANGELOG and also do the relevant versioning via `semver` and creates the relevant git tags.
  - push the generated build artifcats to the Registry or Artifact Repository
  
- Development flow:
  - The user creates a short lived branch
  - The user develops and pushes to the remote branch
  - The CI picks up the changes and then, does the steps above.
  - if it's from the branch then it will do all the build steps and it then pushes it to the `dev` Registry 
  - otherwise if it's from the `main` branch then it will promote this to the `prod` Registry

See: [CI/CD Service Diagram](./diagrams.md#ci--cd-service)

c. Risks/Dangers: I would say the learning curve by developers/engineers who haven't used `Kubernetes`, `docker` (hence Platform As a Service will come into play to `enable` the Engineers/Developers, this will be in a form of tool/framework that abstracts the complexities of the said tools). 


<hr/>

[back](./README.md)
 