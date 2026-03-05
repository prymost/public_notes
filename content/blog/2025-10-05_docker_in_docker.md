+++
title = "Docker in Docker"
date = 2025-10-05

[taxonomies]
categories = ["DevOps"]
tags = ["Docker", "Kubernetes", "Homelab", "DevContainers", "Infrastructure"]
+++

For people who already knew this, it might be trivial, but I learned something interesting last week.

I knew you can run pretty much anything in **Docker**. And I knew Docker with **Compose** or equivalent tools can be used to run a whole dev environment or something like **Testcontainers**. I'd even heard at some point that you can potentially run **Docker inside Docker**, but I either didn't pay attention or had no use for it. And that's what blew my mind when I tried it last week.

As I'm building out my **homelab**, I set up a full **Kubernetes** cluster in a **devcontainer**, and I can easily test new deployments locally. Using my own **YAML** or **Helm**—it doesn't matter. Everything is in a container. The whole **K8s** cluster inside Docker. What? It still blows my mind.

If you want to see how I set it up, check out my [Homelab DevContainer configuration](https://github.com/prymost/homelab/tree/main/.devcontainer) on GitHub.
