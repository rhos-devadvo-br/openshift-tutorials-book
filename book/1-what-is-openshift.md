<br>
<div align="center">
    <a href="../README.md">
        <img width="50%" src="../docs/imgs/rhos-logo.png" alt='rhos-logo'>
    </a>
</div>
<br>
<br>
<br>

# 1. What is Red Hat OpenShift?

## 1.1. Introduction


OpenShift Container Platform is a platform for developing and running containerized applications. It is designed to allow applications and the data centers that support them to expand from just a few machines and applications to thousands of machines that serve millions of clients.

With its foundation in Kubernetes, OpenShift Container Platform incorporates the same technology that serves as the engine for massive telecommunications, streaming video, gaming, banking, and other applications. Its implementation in open Red Hat technologies lets you extend your containerized applications beyond a single cloud to on-premise and multi-cloud environments.

## 1.2. About Kubernetes

Although container images and the containers that run from them are the primary building blocks for modern application development, to run them at scale requires a reliable and flexible distribution system. Kubernetes is the defacto standard for orchestrating containers.

Kubernetes is an open source container orchestration engine for automating deployment, scaling, and management of containerized applications. The general concept of Kubernetes is fairly simple:

- Start with one or more worker nodes to run the container workloads.

- Manage the deployment of those workloads from one or more master nodes.

- Wrap containers in a deployment unit called a pod. Using pods provides extra metadata with the container and offers the ability to group several containers in a single deployment entity.

- Create special kinds of assets. For example, services are represented by a set of pods and a policy that defines how they are accessed. This policy allows containers to connect to the services that they need even if they do not have the specific IP addresses for the services. Replication controllers are another special asset that indicates how many pod replicas are required to run at a time. You can use this capability to automatically scale your application to adapt to its current demand.

In only a few years, Kubernetes has seen massive cloud and on-premise adoption. The open source development model allows many people to extend Kubernetes by implementing different technologies for components such as networking, storage, and authentication.

## 1.3. The benefits of containerized applications

Using containerized applications offers many advantages over using traditional deployment methods. Where applications were once expected to be installed on operating systems that included all their dependencies, containers let an application carry their dependencies with them. Creating containerized applications offers many benefits.

## 1.4. Main differences from Kubernetes

The main difference from Kubernetes is that OpenShift is a full fledged product with enterprise support that requires a paid subscription, while Kubernetes is simply an open-source project. OpenShift Container Platform provides enterprise-ready enhancements to Kubernetes, including the following enhancements:

- Hybrid cloud deployments. You can deploy OpenShift Container Platform clusters to a variety of public cloud platforms or in your data center.

- Integrated Red Hat technology. Major components in OpenShift Container Platform come from Red Hat Enterprise Linux (RHEL) and related Red Hat technologies. OpenShift Container Platform benefits from the intense testing and certification initiatives for Red Hat’s enterprise quality software.

- Open source development model. Development is completed in the open, and the source code is available from public software repositories. This open collaboration fosters rapid innovation and development.

Although Kubernetes excels at managing your applications, it does not specify or manage platform-level requirements or deployment processes. Powerful and flexible platform management tools and processes are important benefits that OpenShift Container Platform offers. In the following image you can see some of the resources and features provided by OpenShift:

<br>
<div align="center">
    <img width="80%" style="1px solid black" src="../docs/imgs/b4-2.png" alt='rhos-components'>
</div>
<br>

OpenShift runs on top of the Red Hat Enterprise Linux CoreOS operating system, and instead of Docker it uses the lightweight CRI-O container engine optimized for OKD. OKD, like most Kubernetes distributions, also uses **Etcd** for key-value pair storage. You can check [more details about the OCP architecture at the official Red Hat documentation](https://access.redhat.com/documentation/en-us/openshift_container_platform/4.5/html/architecture/architecture-rhcos).

OpenShift also has an embedded security layer based on SELinux that disallows the execution of containers as root users, which is one of the main vulnerabilities in containerized applications. OpenShift brings authentication and authorization resources into its object model which Kubernetes currently don't have. In general, OpenShift has a "secure-by-default" policy tailored for Enterprise applications.

Besides security and usability, OpenShift is heavily geared to a DevOps culture, supporting native container image management with the use of an internal Container Image Registry and Image Streams, another type of resource in the OpenShift object model.

>"As a catch-all container platform, Red Hat OpenShift is more than a software product. It can be the key to adopting a DevOps culture, automating routine operational tasks and standardizing environments across an app’s life cycle." — Red Hat

# 1.5. Where can you use it?

Red Hat OpenShift clusters can be "managed" or "self-managed". Managed cluster's compute and network infrastructures are hosted and managed by cloud providers while self-managed clusters needs to be installed from scratch - they can be installed on traditional cloud infrastructure nevertheless. OpenShift is a multicloud offering available at IBM Cloud, Azure, AWS and Google Cloud. A full list of supported cloud providers which have managed OpenShift offerings can be viewed [at the official OpenShift homepage](https://www.openshift.com/products/pricing/).

OpenShift clusters have a monthly license cost attached, while the compute and network infrastructure costs are paid to a specific cloud provider, and vary depending on the allocated resources and specific provider's price plans for infrastructure.

<hr>

[Go to Summary](../README.md)

[Go to Chapter 2: OpenShift Architecture](./2-openshift-architecture.md)