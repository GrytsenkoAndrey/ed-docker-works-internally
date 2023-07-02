# How Docker works internally? Magic Behind Containerization

by [medium.com](https://medium.com/javarevisited/how-docker-works-internally-magic-behind-containerization-65ea5aa0a4ff) article

![1](/img/1.webp)

Hello guys, if you are wondering how Docker works internally but don’t know how then you have come to the right place. In my last article, I explained [How Kubernetes](https://medium.com/javarevisited/how-does-kubernetes-work-internally-702b5d16c6ef) works and in this article, I am going to explain how Docker works.

Along the way, you will also learn about things like how container works, container vs VM, Docker file, Docker image and other Docker related stuff. But, before that a bit of overview of what is Docker and why its important.

In the vast world of modern software development and deployment, Docker has emerged as a powerful tool, revolutionizing the way applications are packaged, shipped, and run across diverse computing environments.

Docker’s popularity stems from its ability to simplify the process of software deployment by leveraging containerization. But how does Docker actually work under the hood?

Earlier, I shared my views on why every developer and DevOps should learn Docker and In this article, we will delve into the internal workings of Docker, unveiling the magic behind this game-changing technology.

This is also an important interview questions for both Developers and DevOps as Kubernetes or K8 is now a days become an essential tool for deploying your app in Cloud.

By the way, If you are preparing for interviews then you will be glad to know that, I have shared several resources for Java interviews like 21 Software Design Pattern questions, 10 Microservice Scenario based questions, 20 SQL queries from Interviews, 50 Microservices questions, 15 System Design Questions, and 35 Core Java Questions and 21 Lambda and Stream questions , if you haven’t checked them yet, I suggest you to look at the them before your interview.

And , if you are not a Medium member then I highly recommend you to join Medium and read great stories from great authors from real field without interruptions. You can join Medium here

## How Docker works internally?

Now that we know what is Docker and what benefits it offer, let’s go into important details one by one.

## 1 What is Containers? How they work?

Before diving into Docker’s internal mechanisms, let’s first grasp the concept of containers. In simple terms, a container is an isolated and lightweight runtime environment that encapsulates an application and its dependencies.

Unlike traditional virtualization, where a full-fledged operating system is emulated, containers share the host system’s kernel, leading to more efficient resource utilization.

Here is a nice diagram which also shows clear difference between Virtual Machine, Hypervisor and Container.

![2](/img/2.webp)

