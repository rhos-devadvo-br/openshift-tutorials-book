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

The output should be like the following:

```bash
Listing installed plug-ins...

Plugin Name                            Version   Status   Private endpoints supported   
container-registry                     0.1.514            false   
container-service/kubernetes-service   1.0.233            false
```

## 3.3. Installing the Kubernetes client (kubectl)

[Download the OpenShift CLI (oc)](https://mirror.openshift.com/pub/openshift-v4/clients/oc/) that matches your local operating system and cluster version. For detailed information about how to install the OpenShift client, [see the docs](https://cloud.ibm.com/docs/openshift?topic=openshift-openshift-cli#cli_oc).

### 3.3.1. For Linux™ users:

TODO

### 3.3.2. For Mac users:

TODO

### 3.3.3. For Windows™ users:

TODO

## 3.4. Installing the OpenShift client (oc)

### 3.4.1. For Linux™ users:

TODO

### 3.4.2. For Mac users:

TODO

### 3.4.3. For Windows™ users:

TODO

