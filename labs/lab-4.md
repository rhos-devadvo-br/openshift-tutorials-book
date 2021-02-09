<br>
<div align="center">
    <a href="../README.md">
        <img width="50%" src="../docs/imgs/rhos-logo.png" alt='rhos-logo'>
    </a>
</div>
<br>
<br>
<br>

# LAB 4: DevOps with Classic Pipelines

## 1. Introduction

In this lab you will create a pipeline to automate the test and deploy process to your Red Hat OpenShift cluster. You will create a pipeline inside IBM Cloud and configure the it to deploy the same Flask application deployed in the provious labs.

## 2. Create a toolchain in IBM Cloud

In your IBM Cloud account access your cluster panel and click in `DevOps` link located in the left side of the screen as shown in the image below.

![lab4-panel](../docs/imgs/lab4-clusterpanel.png)

The page loaded has all the toolchains that deploy some application to the selected cluster. To create a new toolchain just click in the `Create toolchain` button locared in the top rigth coner as displayed in the image below.

![lab4-devops](../docs/imgs/lab4-tool.png)

Once you clicked, should appear the catalog of toolchains. There you will find options of pipeline of deployment with many diferent features, for now you will use `Develop a Kubernetes app` as you can se below.

![lab4-catalogtool](../docs/imgs/lab4-catalogtool.png)

Now you are at configuration form the toolchain. It is important you select the provider of the code as `GitHub` keep the pipeline type as `Classic`. If you are fulfilling this form for the firt time, the platform will ask your athorization to perform github operation like clone the repo. The source repository URL show be: `https://github.com/rhos-devadvo-br/pymongo-demo.git`

![lab4-create](../docs/imgs/lab4-create.png)

After fulfill the github section you must complete the `Delivery Pipeline` section. You have to create a new `APIKEY` by clicking in `New` button and then make sure the target is the correct cluster. With all the form correct just hit the `Create` button as shown in the image below.

![lab4-cd](../docs/imgs/lab4-cd.png)

You shall see all card that compose the toolchain. The integration with GitHub and the delivery pipeline. To watch the deployment steps just click over the `Delivery Pipeline` card as displayed in the image below.

![lab4-pipeline](../docs/imgs/lab4-pipeline.png)

Now you can see all the stages of the deployment process. Firts clone the original repository to you GutHub account, then start to build the application imagem and finally deploy the image in the cluster. These cards are the base. In time, when you get more skilled you can add other cards to test the app in a diferent environment and certify the app, but for now you know how to the basics.

![lab4-card](../docs/imgs/lab4-card.png)

When the process finish you will see all the cards with a green tab over the card like the image below.

![lab4-done](../docs/imgs/lab4-done.png)

To see your application running, as you have seen before, access you cluster and select the same project you have created during the `Delivery Pipeline` section. Here it is.

![lab4-app](../docs/imgs/lab4-app.png)

To make your app accesible from your internet browser you have to change the view to admin and select the `Network` tab, then click on `Routes`.

![lab-network](../docs/imgs/lab4-network.png)

On the top right coner hit the `Create Route` button.

![lab4-route](../docs/imgs/lab4-route.png)

In the form give a name to the route, select the service of your application and then the target port to be released and finally click on `Create` button.

![lab4-release](../docs/imgs/lab4-release.png)

Once you did that return to the Developer view and hit the link button on the app visualization.

![lab4-finish](../docs/imgs/lab4-finish.png)

And now you have complete the lab.

![lab4-complete](../docs/imgs/lab4-complete.png)

<hr>

[Go to LAB 3: DevOps with OpenShift source-to-image (s2i) and GitHub webhooks](./lab-3.md)

[Go to LAB 5: --](./lab-5.md)