## Tech Stack

* `AWS` Services:
  * [EKS](https://aws.amazon.com/eks/) for hosting the API and for container orchestration.
    * [EKS Blueprint](https://aws.amazon.com/blogs/containers/bootstrapping-clusters-with-eks-blueprints/) OOTB from `AWS`
  * [API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html) for handling `API` Requests and Endpoints
  * [Cognito](https://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html) for handling Auth Tokens and Security
  * [Application LoadBalancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html) additional layer of security.
  * [WAF](https://aws.amazon.com/waf/) additional layer of security.
* [CDK](https://aws.amazon.com/cdk/) for IaC
* [devspace](https://www.devspace.sh/) or [tilt](https://tilt.dev/) for local development.
* [LocalStack](https://www.localstack.cloud/) for local development emulating AWS Services 
* [GitHub Actions](https://github.com/features/actions) for CI (Application and Infrastructure) and CD for Infrastructure.
* [ArgoCD](https://argo-cd.readthedocs.io/en/stable/) for CD (Application).
* [Helm](https://helm.sh/) for Deployment Manifest.

<hr/>

[back](./README.md)