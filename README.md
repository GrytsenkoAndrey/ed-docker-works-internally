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

## 2 Docker Architecture

At the core of Docker’s architecture is a client-server model that consists of three key components: the Docker client, the Docker daemon, and the Docker registry.

The Docker client acts as the primary interface through which users interact with Docker, while the Docker daemon is responsible for building, running, and managing containers.

The Docker registry serves as a centralized repository for storing Docker images, which are the building blocks for containers. It’s similar to NPM which host node packages or Maven repository which stores JAR files for many Java libraries.

Here is a nice diagram from Whizlabs which shows how Docker works and how images are pulled from registry during Docker build process.

![3](/img/3.webp)

## 3 Images and Layers

To truly understand Docker’s inner workings, we need to explore the concept of Docker images.

An image is a read-only template that contains everything needed to run an application, including the code, runtime environment, libraries, and dependencies.

Docker images are built using a layered file system, with each layer representing a change or modification made to the image. This layering mechanism allows for efficient storage and sharing of common components across multiple images, reducing redundancy and improving performance.

Here is another nice diagram which explains the relationship between Docker file, Docker Image and Docker Container:

![4](/img/4.webp)

## 4 The Dockerfile

The Dockerfile acts as a blueprint for building Docker images. It is a text file that specifies the instructions needed to create an image. These instructions include defining the base image, adding dependencies, copying files, exposing ports, and executing commands during the image build process.

Docker intelligently caches intermediate layers based on the Dockerfile instructions, speeding up subsequent builds and minimizing redundancy.

Here is a sample of DockerFile you can see the content:

![5](/img/5.webp)

## 5 Container Runtimes

When a Docker image is run, it is instantiated as a container using a container runtime. Docker supports multiple container runtimes, with Docker Engine (using the default runtime called runc) being the most common.

The container runtime creates an isolated environment, sets up namespaces, allocates resources, manages networking, and controls access to system resources, ensuring containers remain isolated from each other and the host system.

![6](/img/6.webp)

## 6 Container Orchestration and Networking

Docker’s versatility extends beyond running individual containers. It provides powerful orchestration tools, such as Docker Swarm and Kubernetes, that enable the management of containerized applications at scale.

These tools facilitate the deployment, scaling, and load balancing of containers across a cluster of machines, ensuring high availability and fault tolerance.

Docker also provides networking capabilities, allowing containers to communicate with each other and the outside world through virtual networks, ports, and routing.

Here is a nice diagram of using containers at scale:

![7](/img/7.webp)

## Conclusion

That’s all about how Docker works internally. Docker has fundamentally transformed the way we develop, package, and deploy software applications.

By understanding its internal workings, we gain insights into the underlying technology that has brought containerization to the forefront of modern software engineering. From the client-server architecture to the layered image system and container runtimes, Docker’s elegant design and powerful features make it an indispensable tool for developers and operations teams worldwide.

As the world of software continues to evolve, Docker remains at the forefront, enabling efficient and scalable application deployment in an ever-changing landscape.

As I said before, this is also an important topic for interviews and knowing How Docker works can help you showcase your skill on interview as well.

By the way, if you are preparing for interviews then along with this, you can also prepare questions like [difference between API Gateway and Load Balancer](https://medium.com/javarevisited/difference-between-api-gateway-and-load-balancer-in-microservices-8c8b552a024), Kafka vs RabbitMQ, [JWT vs OAuth](https://medium.com/javarevisited/difference-between-jwt-oauth-and-saml-for-authentication-and-authorization-in-web-apps-75b412754127), how to manage transactions in Microservices, and difference between SAGA and CQRS Pattern as well, they are quite popular on interviews.
