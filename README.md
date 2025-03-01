![Build Status](https://img.shields.io/github/workflow/status/aws/karpenter/CI/main)
![GitHub stars](https://img.shields.io/github/stars/aws/karpenter)
![GitHub forks](https://img.shields.io/github/forks/aws/karpenter)
[![GitHub License](https://img.shields.io/badge/License-Apache%202.0-ff69b4.svg)](https://github.com/aws/karpenter/blob/main/LICENSE)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/aws/karpenter/issues)

![](website/static/banner.png)

Karpenter is an open-source node provisioning project built for Kubernetes.
Its goal is to improve the efficiency and cost of running workloads on Kubernetes clusters.
Karpenter works by:

* **Watching** for pods that the Kubernetes scheduler has marked as unschedulable
* **Evaluating** scheduling constraints (resource requests, nodeselectors, affinities, tolerations, and topology spread constraints) requested by the pods
* **Provisioning** nodes that meet the requirements of the pods
* **Scheduling** the pods to run on the new nodes
* **Removing** the nodes when the nodes are no longer needed

For most use cases, a cluster’s capacity can be managed by a single Karpenter Provisioner.
However, you can define multiple Provisioners, enabling use cases like isolation, entitlements, and sharding.
Using a combination of defaults and overrides, Karpenter determines the availability zone, instance type, capacity type, machine image, and scheduling constraints for pods it manages.

Come discuss Karpenter in the [#provider-aws channel](https://kubernetes.slack.com/archives/C0LRMHZ1T) in the [Kubernetes slack](https://slack.k8s.io/)!

Check out the [Docs](https://karpenter.sh/) to learn more.

## Installation

Follow the setup recommendations of your cloud provider.
- [AWS](https://karpenter.sh/docs/getting-started/)

> ❗ Note: There may be backwards incompatible changes between versions when upgrading before v0.3.0. Karpenter follows [Kubernetes versioning guidelines](https://kubernetes.io/docs/concepts/overview/kubernetes-api/#api-changes). Before upgrading, we recommend:
> - Check the [release notes](https://github.com/aws/karpenter/releases)
> - Uninstall Karpenter
> - Remove all nodes launched by karpenter
> - Reinstall Karpenter

## References
- [Docs](https://karpenter.sh/docs/)
- [Concepts](https://karpenter.sh/docs/concepts/)
- [API](https://karpenter.sh/docs/provisioner/)
- [Working Group](WORKING_GROUP.md)
- [Developer Guide](https://karpenter.sh/docs/development-guide/)
- [Contributing](CONTRIBUTING.md)

## Talks
- 12/20/2021 [How To Auto-Scale Kubernetes Clusters With Karpenter](https://youtu.be/C-2v7HT-uSA)
- 11/30/2021 [Karpenter vs Kubernetes Cluster Autoscaler](https://youtu.be/3QsVRHVdOnM)
- 11/19/2021 [Karpenter @ Container Day](https://youtu.be/qxWJRUF6JJc)
- 05/14/2021 [Groupless Autoscaling with Karpenter @ Kubecon](https://www.youtube.com/watch?v=43g8uPohTgc)
- 05/04/2021 [Karpenter @ Container Day](https://youtu.be/MZ-4HzOC_ac?t=7137)

## License
This project is licensed under the Apache-2.0 License.
