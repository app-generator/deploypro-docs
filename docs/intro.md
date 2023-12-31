---
sidebar_position : 0
title            : DeployPRO, The Service
sidebar_label    : Intro
slug             : /
description      : The official documentation of the service. 
---

<!-- GOOGLE Stuff -->
<head>
    <meta name="google-site-verification" content="VW84QZUx9lXlONq9YSMvPLpJyY0w-ZSutA89XdGT7xo" />
</head>

Introducing [DeployPRO](https://deploypro.dev/), a product that aims to simplify the deployment process, 
empowering businesses to deploy, monitor, and scale applications without the burden of infrastructure complexities. 

Works with all major cloud providers like **[AWS](aws/intro)**, **[Azure](azure/intro)**, **[App Platform](app-platform-do/intro)** (DO), and **GCP** (soon). 

With [DeployPRO](https://deploypro.dev/), you can effortlessly create and manage applications, gaining full control of your development process. 
Experience the power and flexibility of **DeployPRO** as it leads you to streamlined and hassle-free cloud deployment.

![DeployPRO - Splash Screen.](https://user-images.githubusercontent.com/51854817/263670372-9a969620-d92d-400b-81ca-bd80f3985bc5.jpg)

<br />

## ✅ How it Works 

Once the users are [authenticated](https://deploypro.dev/signin/) using their **GitHub** account, the first step is to connect at least one Cloud Provider. 

With one of **[AWS](aws/intro)**, **[Azure](azure/intro)**, or **[App Platform](app-platform-do/intro)** activated, the users are able to create VPS servers and trigger deployments for every GitHub repository with a Dockerfile. 

The current version of `DeployPRO` requires a **Dockerized** project in order to have a successful deployment, and it is also essential to mention that `only Dokerfiles are supported` ( using docker-compose.yml won't work).

In summary, here are the benefits using **DeployPRO** service:

- Manage the VPS servers (create, delete) on AWS, Azure, and DO
- Deploy any repository using GitHub Actions (created by DeployPRO)
- Works with Public and Private Repositories 
- SSL by CertBot 
- All deployed applications are enhanced with active CI/CD flows 

<br />

## ✅ Full Sample for AWS

In this demonstration, we will use an open-source sample generated by **Rocket Generator**, a free service that [Generates Django Starters](https://app-generator.dev/).

> [Django Soft Dashboard](https://github.com/app-generator/sample-rocket-django-aws) - `open-source` starter

Here are all the steps to deploy a Django Project   

- Access [DeployPRO](https://deploypro.dev/) and register using `GitHub`
- Connect your **AWS** account using account credentials 
- Create a new VPS Server and wait the full deployment (usually takes = 5min)
- Fork this sample and create a new APP
  - https://github.com/app-generator/sample-rocket-django-aws
- Complete the deployment form
  - NOTE: Needs to have a `Dokerfile` inside
- Confirm the deployment 
- Access the GitHub repository and monitor the progress (GitHub Actions)
- Visit the app in the browser. 

At this point, the app is Deployed LIVE using a new DeployPRO subdomain, but the users can attach a domain.  

<br />

### Access [DeployPRO](https://deploypro.dev/)

The service allows the registration using GitHub (no password required)

![DeployPRO - Registration Page](https://user-images.githubusercontent.com/51854817/263670395-cf095113-c0b1-44ab-91ef-1ca4fc871ead.jpg)
 
<br />

### Connect AWS 

In the `connections` page, users can connect to AWS via credentials. 

![DeployPRO - AWS Credentials](https://user-images.githubusercontent.com/51854817/263670354-2b1dd20b-4874-49f7-a97a-44f8703bb27d.jpg)

If the operation is successfull, the connection to AWS is flagged as active. 

![DeployPRO - AWS Connection Active](https://user-images.githubusercontent.com/51070104/263734577-6c32142f-0d88-4d52-8680-1bcc725c376b.png)

<br />

### Create new Server 

Before deploying the project, a deployment server needs to be created (operation usually takes ~5 min). 

![DeployPRO - Create AWS Server](https://user-images.githubusercontent.com/51854817/263670373-dd12a0da-48b9-4954-8440-3768bdd97083.jpg)

<br />

Once created, we can access the default page and also check out the details in our AWS account: 

![DeployPRO - AWS Server, the default page.](https://user-images.githubusercontent.com/51854817/263670388-5f9d2579-2112-4f12-afe8-e19017c9ee8b.jpg)

<br />

> Server Information (AWS) 

![DeployPRO - New AWS Server (on AWS)](https://user-images.githubusercontent.com/51854817/263670337-91e8bb53-59c3-4256-b25b-76b178c68f1c.jpg)

<br />

The server state can be also checked on DeployPRO. 

![DeployPRO - New AWS Server (on DeployPRO)](https://user-images.githubusercontent.com/51070104/264061233-a464745e-d89e-4cb5-b6c8-7f6e6dffc406.png)

<br />

### [Deploy Django on AWS](https://github.com/app-generator/sample-rocket-django-aws)

In this phase, the user needs to provide:

- the repository 
- app name 
- path to the [Dockerfile](https://github.com/app-generator/sample-rocket-django-aws/blob/main/Dockerfile)
- the PORT exposed in Docker (execution entry point)
  - For this project the is `PORT=5005`
- the `DeployPRO` subdomain 

![DeployPRO - AWS & Django, App information](https://user-images.githubusercontent.com/51854817/263670396-d5a7f163-e637-4289-a7a2-2359825ef941.jpg)

---

![DeployPRO - AWS & Django, App information in Full](https://user-images.githubusercontent.com/51854817/263670408-e3494989-0e24-4acb-98ea-1b99ded04900.jpg)

Once the operation is confirmed, DeployPRO will analyze the input and update the repository with all the necessary scripts for the LIVE deployment. 

![DeployPRO - Deploy Django on AWS, via GitHub Action.](https://user-images.githubusercontent.com/51070104/263740098-12517c63-b809-4615-b8b1-b2d45f6fa6d9.png)

<br />

---

![DeployPRO - Deploy Django on AWS (GitHub Action) CI-CD flow completed.](https://user-images.githubusercontent.com/51070104/263740916-c63215b1-a476-4377-81f6-78da3e17de74.png)

<br />

### Access the APP (browser)

At this point, the Django App should be fully deployed on AWS, with an active CI/CD flow: 

![DeployPRO - Django Starter fully deployed on AWS (CI/CD flow active)](https://user-images.githubusercontent.com/51854817/263670401-214ac050-69c2-472d-96f4-b914dc464e6f.jpg)

<br />

## ✅ Feedback

What are the ways to offer feedback? 📝

Please use our [GitHub Issues](https://github.com/app-generator/deploypro/issues).  
If you come across anything that appears unclear, kindly inform us, so we can address it appropriately!

<br />

## ✅ Resources

- 👉 [Deploy Projects](https://deploypro.dev/) using your preferred provider: `AWS`, `DigitalOcean`, `Azure`, and GCP (soon)
- 👉 Get [Deployment Support](https://deploypro.dev/support/) from the team behind this service
- 👉 Join the [Community](https://discord.gg/qQhjQZhnur) and chat with the team behind `DeployPRO`
