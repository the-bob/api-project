## CI/CD


### Service 

* Service:
  * CI: `GitHub Actions` and the steps are detailed under section `b` in the `Task` Section.
  * CD: `GitOps` Approach using `ArgoCD` that is `OOTB` from `AWS EKS Blueprint`

see [Diagram](./diagrams.md#ci--cd-service)

### Infrastructure

* Infra:
  * CI: `GitHub Actions` - Steps are almost identical as the service barring the `Dockerization` part.
  * CD: `GitHub Actions` - we'll go with a push based deployment rather than pull based. This will ensure that any changes in the infra is a conscious decision by the Engineers.

see [Diagram](./diagrams.md#ci--cd-service)

<hr/>

[back](./README.md)