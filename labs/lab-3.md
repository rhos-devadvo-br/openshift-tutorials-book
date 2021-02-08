<br>
<div align="center">
    <a href="../README.md">
        <img width="50%" src="../docs/imgs/rhos-logo.png" alt='rhos-logo'>
    </a>
</div>
<br>
<br>
<br>

# LAB 3: DevOps with OpenShift source-to-image (s2i) and GitHub webhooks

## 1. Introduction

In this lab you'll make use of the GitHub webhook functionality to allow OpenShift to detect commit pushes automatically. These detections will trigger the build of the updated code and then the continuous deployment of the Flask web application built on [LAB 1](./lab-1.md) and [LAB 2](./lab-2.md). This capability is called source-to-image (s2i).

## 2. Configuring the GitHub webhook

Go to the Administrator panel and "Builds -> Build Configs" then click on the "web" BuildConfig created at LAB 1.

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-1.png" alt='webhook-1'>
</div>
<br>

You'll see information about the created Deployment, such as the source Git Repository, Build image templates and labels. Scrolling to the end of the page you'll see URLs that can be used to configure webhooks.

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-2.png" alt='webhook-2'>
</div>
<br>

Copy the GitHub webhook URL and navigate to the GitHub source repository settings.

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-github-1.png" alt='webhook-github-1'>
</div>
<br>

Click at the "Webhooks" tab on the left-side panel.

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-github-2.png" alt='webhook-github-2'>
</div>
<br>

Then at the top-right corner click on "Add webhook".

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-github-3.png" alt='webhook-github-3'>
</div>
<br>

Paste the webhook URL at the "Payload URL" field, select "application/json" in the "Content type" drop-down menu and then click on the green "Add webhook" button.

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-github-4.png" alt='webhook-github-4'>
</div>
<br>

GitHub should display a light-blue message on the top of the page saying that the webhook was successfully configured, as shown in the picture below.

<br>
<div align="center">
    <img width="100%" style="border: 1px solid black" src="../docs/imgs/webhook-github-5.png" alt='webhook-github-1'>
</div>
<br>

## 3. Pushing a new commit to the repository

After the webhook configuration is done you can edit any part of the code and OpenShift will automatically start building the updated version of the application as soon as the commit is pushed to the source repository.

Note: if your GitHub repository is private, you'll need to configure a SourceSecret at your GitHub project. This can be done in the application creation form at the "Advanced github options" tab.

<hr>

[Go to LAB 2: Scaling pods and adding a self-healing database layer with a Template](./lab-2.md)

[Go to LAB 4: --- ](./lab-4.md)