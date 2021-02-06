# ibmcloud-ocp-101

## Leading Multicloud Container Development Platform

Red Hat OpenShift is named a leader across 29 criteria and 8 major vendors by the [Q3 2020 Forrester Wave report](https://www.openshift.com/2020-forrester-wave?hsLang=en-us).

## Red Hat OpenShift offerings and costs

Red Hat OpenShift clusters can be "managed" or "self-managed". Managed cluster's compute and network infrastructures are hosted and managed by cloud providers while self-managed clusters need to be installed from scratch - they can be installed on traditional cloud infrastructure nevertheless. A full list of supported cloud providers which have managed OpenShift offerings can be viewed [at the official OpenShift homepage](https://www.openshift.com/products/pricing/).

OpenShift clusters have a Red Hat monthly license cost attached, while the compute and network infrastructure costs are paid to a specific cloud provider and vary depending on the allocated resources and specific provider's price plans.

## Creating a managed OpenShift cluster at IBM Cloud

There are two types of managed OpenShift clusters "as a Service" at IBM Cloud: a cluster created with classic infrastructure, or one created with a Virtual Private Cloud (VPC) infrastructure. VPC clusters have a virtual network layer built on top of the Virtual Servers Instances (VSI's). This network layer provides isolation and improved personalization capabilities such as custom network security policies for the subjacent compute infrastructure. VPC infrastructure is not yet available at South America.

- [Provison a Virtual Private Cloud](https://cloud.ibm.com/vpc/provision/vpc) (Optional)
- [Provison a managed OpenShift cluster](https://cloud.ibm.com/kubernetes/catalog/create?platformType=openshift)

If you choose to create a VPC cluster you need to have at least three subnets (one in each AZ). When provisoning the OpenShift cluster at IBM Cloud, you'll setup the following:

- OpenShift version (3.11, 4.4, or 4.5)
- Purchase of additional OCP licenses or application of an existing Cloud Pak OCP entitlement license
- Infrastructure type: Classic, VPC, or Satellite (new)
- Location (AZs and subnets)
- Worker Pool (vCPUs, Memory, nº of worker nodes)

## Accessing your cluster

At the [IBM Cloud Resources List](https://cloud.ibm.com/resources) click on the previously created cluster. You'll be redirected to the managed cluster administration page at IBM Cloud, where you can check access, overview worker node's status, create new worker pools, install add-ons and attach IBM DevOps solutions to your cluster.

### Using the Web Console

### Using the OpenShift CLI (oc)

[Download the OpenShift CLI (oc)](https://mirror.openshift.com/pub/openshift-v4/clients/oc/) that matches your local operating system and cluster version. For information about how to install the CLI, [see the docs](https://cloud.ibm.com/docs/openshift?topic=openshift-openshift-cli#cli_oc). For OpenShift 4.5 check [this link](https://mirror.openshift.com/pub/openshift-v4/clients/oc/4.5/).


