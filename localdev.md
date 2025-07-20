## Developer Experience

In order to assist our Developers for this setup:

* We'll use either `devspace` or `tilt`
  * The mentioned tools will help developers work in a `Container` Centric approach, they can develop locally against a `Kubernetes` Cluster, be it using `minikube`, `k3s`, `Rancher Desktop` etc. or if we have the luxury of provisioning `ephemeral` clusters in the Cloud then the said tools have the ability in doing so.
* Also the use of `Local Stack` that will help the Engineers in having a locally emulated `AWS Service`
* CI - As part of the offering, the Git Repo in `GitHub` will have a `GitHub Actions Workflow`

*NOTE:* By chosing `Docker` and `devspace/tilt`, this will potentially minimise the scenario of "It works on my machine".  And will make it easier to develop on an almost identical production environment.

<hr/>

[back](./README.md)
