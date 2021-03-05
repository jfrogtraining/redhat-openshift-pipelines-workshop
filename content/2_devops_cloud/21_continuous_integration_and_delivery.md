---
title: "Continuous Integration and Delivery"
chapter: false
weight: 21
pre: "<b>2.1 </b>"
---

![CICD](/images/cicd.png)

Continuous integration and delivery (CI/CD) is the process for which your software components are built from code, integrated, tested, released, deployed and ultimately delivered to end-users. CI/CD pipelines are the software assembly line that orchestrates the building of your software. This CI/CD pipeline line requires infrastructure. Cloud computing has allowed this infrastructure to become dynamic and ephemeral. On cloud infrastructure, your CI/CD pipelines scale up and down to meet your software delivery demands. It saves costs by providing the right amount of cloud infrastructure just as it is needed. This is further realized by using cloud-native technologies like Kubernetes and extending across clouds and on-premise datacenters. The following are some Red Hat Openshift cloud technologies that CI/CD pipelines can utilize:

- Red Hat Openshift Virtual Machines can be used as CI/CD pipeline nodes that can be dynamically spun up and down to execute pipeline tasks.
- Red Hat Openshift Spot Virtual Machines can dramatically lower costs by utilizing spare capacity nodes for CI/CD pipeline tasks.
- Red Hat Openshift Kubernetes Service (AKS) can provide a Kubernetes-based CI/CD worker node pools and allow more efficient use of compute resources.
- Red Hat Openshift Stack can allow you to span your CI/CD pipelines from your on-premise datacenter to the cloud for hybrid and migration use cases.



