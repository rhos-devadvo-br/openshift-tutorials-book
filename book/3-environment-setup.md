<br>
<div align="center">
    <a href="../README.md">
        <img width="50%" src="../docs/imgs/rhos-logo.png" alt='rhos-logo'>
    </a>
</div>
<br>
<br>
<br>

# 3. Environment Setup

Before starting the labs, you must first install the following tools:

* IBM Cloud CLI (ibmcloud)
* The **container-registry** plugin for IBM Cloud CLI
* The **kubernetes-service** plugin for IBM Cloud CLI
* The Kubernetes client (kubectl)
* The OpenShift client (oc)

## 3.1. Installing the IBM Cloud CLI

### 3.1.1. For Linux™ users:

For Linux™, copy and paste the following command to a terminal and run it:

```bash
curl -fsSL https://clis.cloud.ibm.com/install/linux | sh
```

### 3.1.2. For Mac users:

For Mac, copy and paste the following command to a terminal and run it:

```bash
curl -fsSL https://clis.cloud.ibm.com/install/osx | sh
```

### 3.1.3. For Windows™ users:

For Windows™, copy and paste the following command to a Windows™ PowerShell terminal console and run it:

```powershell
iex(New-Object Net.WebClient).DownloadString('https://clis.cloud.ibm.com/install/powershell')
```
If you encounter errors like `The underlying connection was closed: An unexpected error occurred on a send`, make sure you have .Net Framework 4.5 or later installed. Also try to enable TLS 1.2 protocol by running the following command:

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
```

## 3.2. Installing the IBM Cloud CLI required plugins

Log in the IBM Cloud CLI and setup the IBM Cloud Region, Resource Group and Cloud Foundry API endpoint, Org and Space. This can be done using the following command:

```bash
ibmcloud target -r <region> -g <resource_group> --cf
``` 

List the available plugins for IBM Cloud CLI with the command:

```bash
ibmcloud plugin repo-plugins
```

Install the **container-registry** and **kubernetes-service** plugins:

```bash
ibmcloud plugin install container-registry
```

```bash
ibmcloud plugin install kubernetes-service
```

Check if the plugins were installed correctly using plugin list:

```bash
ibmcloud plugin list
```

Example output:

    Listing installed plug-ins...

    Plugin Name                            Version   Status   Private endpoints supported   
    container-registry                     0.1.514            false   
    container-service/kubernetes-service   1.0.233            false


## 3.3. Installing the Kubernetes (kubectl) and OpenShift (oc) command-line clients

Red Hat OpenShift at IBM Cloud is available in different versions (not always the latest release by Red Hat). To check the release history, visit the [IBM official documentation](https://cloud.ibm.com/docs/openshift?topic=openshift-openshift_versions#openshift_release_history).

Currently supported versions of Red Hat OpenShift at IBM Cloud:

    Latest: 4.6 (requires Kubernetes 1.19)
    Default: 4.5 (requires Kubernetes 1.18)

Deprecated and unsupported versions:

    Deprecated: 3.11 (requires Kubernetes 1.11), 4.4 (requires Kubernetes 1.17)
    Unsupported: 4.3 (requires Kubernetes 1.16)

To install the OpenShift 4.x client (oc) and kubectl, you must first download the tar/zip files corresponding to your cluster version from mirror.openshift.com.

* For OpenShift 4.x: https://mirror.openshift.com/pub/openshift-v4/clients/oc/

Make sure you download the correct files for your Operational System (if using Linux, make sure you select the correct architecture). In the next subsections we present instructions on how to install `oc` and `kubectl`.

### 3.3.1. For Linux™ users:

After downloading the correct .tar file, unpack it:

```bash
tar -xvf oc.tar.gz
```

The `kubectl` and `oc` executables will be unpacked to the current directory. To add these binary files into your PATH system variable, execute the following (you may need *sudo* or administrator permissions):

```bash
mv ./oc /usr/local/bin/oc && mv ./kubectl /usr/local/bin/kubectl && echo $PATH
```

To check if the OpenShift command-line client (oc) was installed correctly, run:

```bash
oc version
```

Example output: 

```bash
Client Version: 4.6.19
```

To check if the Kubernetes command-line client (kubectl) was installed correctly, run:

```bash
kubectl version
```

Example output: 

    Client Version: version.Info{Major:"1", Minor:"19", GitVersion:"v1.19.0", GitCommit:"aaa9ca377e9816a2501ce3f5dda3f889618b6a37", GitTreeState:"clean", BuildDate:"2021-02-20T03:33:06Z", GoVersion:"go1.15.5", Compiler:"gc", Platform:"linux/amd64"}

### 3.3.2. For Mac users:

TODO

### 3.3.3. For Windows™ users:

TODO

<hr>

# Extra content

* [Red Hat OpenShift on IBM Cloud CLI commands](https://cloud.ibm.com/docs/openshift?topic=openshift-kubernetes-service-cli)