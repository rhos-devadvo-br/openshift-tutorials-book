<br>
<div align="center">
    <img width="50%" src="../docs/imgs/rhos-logo.png" alt='rhos-logo'>
</div>
<br>
<br>
<br>

# 1. What is Red Hat OpenShift?

# 1.1. Introduction

Red Hat OpenShift Container Platform is an Enterprise Product focused on IT operations and cloud-native applications development. OpenShift is based on an optimized Kubernetes distribution called [OKD](https://www.okd.io/) that adds developer and operations-centric tools on top of Kubernetes to enable rapid application development, easy deployment and scaling, and long-term lifecycle maintenance for small and large teams. OKD is free to use and has the core features of OpenShift, but without the enterprise support that comes with the paid Red Hat OpenShift subscription. OpenShift, like OKD and Kubernetes, is also completely open-source. You can see the code for yourself at [GitHub](https://github.com/openshift/).

Red Hat OpenShift is named a leader across 29 criteria and 8 major vendors by the [Q3 2020 Forrester Wave report](https://www.openshift.com/2020-forrester-wave?hsLang=en-us).

# 1.2. Main differences from Kubernetes

The main difference from Kubernetes is that OpenShift is a full fledged product with enterprise support that requires a paid subscription, while Kubernetes is simply an open-source project. OpenShift has Kubernetes (the OKD distribution) as one of it's internal components, as it can be noted from the picture below.

<br>
<div align="center">
    <img width="60%" style="1px solid black" src="../docs/imgs/rhos-components.png" alt='rhos-components'>
</div>
<br>

OpenShift runs on top of the Red Hat Enterprise Linux CoreOS operating system, and instead of Docker it uses the lightweight CRI-O container engine optimized for OKD. OKD, like most Kubernetes distributions, also uses ETCD for key-value pair storage. You can check [more details about the OCP architecture at the official Red Hat documentation](https://access.redhat.com/documentation/en-us/openshift_container_platform/4.5/html/architecture/architecture-rhcos).


TO DO:

- Security
- Operators
- DevOps

# 1.3. Where can you use it?

Red Hat OpenShift clusters can be "managed" or "self-managed". Managed cluster's compute and network infrastructures are hosted and managed by cloud providers while self-managed clusters needs to be installed from scratch - they can be installed on traditional cloud infrastructure nevertheless. OpenShift is a multicloud offering available at IBM Cloud, Azure, AWS and Google Cloud. A full list of supported cloud providers which have managed OpenShift offerings can be viewed [at the official OpenShift homepage](https://www.openshift.com/products/pricing/).

OpenShift clusters have a monthly license cost attached, while the compute and network infrastructure costs are paid to a specific cloud provider, and vary depending on the allocated resources and specific provider's price plans for infrastructure.

You can learn how to provision an OpenShift cluster on IBM Cloud at [section 2 of this lab](./2-roks-at-ibm-cloud.md).
