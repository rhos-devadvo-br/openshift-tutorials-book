<br>
<div align="center">
    <a href="../README.md">
        <img width="50%" src="../docs/imgs/rhos-logo.png" alt='rhos-logo'>
    </a>
</div>
<br>
<br>
<br>

# LAB 7: Horizontal Pod auto-scaling

## 1. Introduction

Horizontal Pod auto-scaling can be attained with the declaration of HorizontalPodAutoscalers (HPA) objects. These objects are able to scale-out or scale-in the number of Pods inside a Deployment based on a pre-defined metric. OpenShift supports two types of metric for configuring HPAs: CPU and Memory utilization.

## 2. Deploying the sample microsservice

Create a new OpenShift Project named hpa-demo.

```bash
oc new-project hpa-demo
```

Then create a new Application called hpa-app, using the sample Go-Lang code provided here: https://github.com/rhos-devadvo-br/horizontal-autoscaler-demo.

```bash
oc new-app 'https://github.com/rhos-devadvo-br/horizontal-autoscaler-demo' --name=hpa-app
```

OpenShift will automatically select the tailored Go container image from the Red Hat catalog and deploy the sample microsservice.

Expose the created application with a Route:

```bash
oc expose service/hpa-app
```

## 2. Creating a HPA with the OpenShift CLI

Run the following command to create the autoscaler. This will create an HPA that maintains between 1 and 10 replicas of the Pods controlled by the hpa-app Deployment created. Roughly speaking, the HPA will increase and decrease the number of replicas to maintain an average CPU utilization across all Pods of 80% (since each pod requests 50 millicores, this means average CPU usage of 40 millicores)

```bash
oc autoscale deployment/hpa-app --cpu-percent=80 --min=1 --max=10
```

## --- TO DO

<hr>

[Go to LAB 6: The Canary and Blue-Green release approaches](./lab-6.md)

[Go to LAB 8: --](./lab-8.md)
