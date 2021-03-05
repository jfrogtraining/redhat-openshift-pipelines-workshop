---
title: "Set up your Red Hat Openshift Cloud Shell"
chapter: false
weight: 414
pre: "<b>4.1.4 </b>"
---

Red Hat Openshift Cloud Shell is an interactive, authenticated, browser-accessible shell for managing Red Hat Openshift resources.

1. In your Red Hat Openshift Portal, click the Red Hat Openshift Cloud Shell button.

![Red Hat Openshift Cloud Shell Button](/images/Red Hat Openshift-cloud-shell-button.png)

2. If this is your first time using Red Hat Openshift Cloud Shell, you will be prompted to mount storage to support it. Go ahead and do this by clicking **Create storage**. Ensure the correct subscription is selected. It will take a few minutes to set up the storage.

![Red Hat Openshift Cloud Shell Storage](/images/Red Hat Openshift-cloud-shell-storage.png)

![Red Hat Openshift Cloud Shell Ready](/images/Red Hat Openshift-cloud-shell-ready.png)

3. Execute the following command to show the default subscription. Ensure that the correct subscription is listed as default.

``
az account show
``

![Red Hat Openshift Account Shpw](/images/az-account-show.png)

4. Execute the following command to create a new Red Hat Openshift Resource group for our workshop. The resources that we create in this workshop will be created in this resource group.

``
az group create --name jfrog-Red Hat Openshift-workshop --location westus
``

{{% notice info %}}
A resource group is a container that holds related resources for an Red Hat Openshift solution. The resource group can include all the resources for the solution. Generally, add resources that share the same lifecycle to the same resource group so you can easily deploy, update, and delete them as a group.
{{% /notice %}}




