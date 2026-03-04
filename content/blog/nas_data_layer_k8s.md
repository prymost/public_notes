+++
title = "Using NAS as a Data Layer for K8s"
date = 2025-11-16

[taxonomies]
categories = ["Homelab"]
tags = ["NAS", "NFS", "Kubernetes", "K8s", "Data Persistence", "Backups"]
+++

I have only had time this week for a tiny personal project. And that project was to use my **NAS** as a data persistence layer for at least some of the apps running in my **K8s cluster**. It was surprisingly easy.

The setup required tinkering with nodes and **K8s** manifests, but it all went very smoothly. So now I have my **Minecraft** server storing all the data on my NAS via **NFS**, so even if my lab's hardware fails, the data will not be lost. And as I'm running backups on the NAS itself, I can protect the data even more.

There is a tiny latency tradeoff. I did notice a bit of a lag in Minecraft, as it has to read and write files a lot. But because all connections are wired and the lab and NAS are on the same switch, it has not been a problem so far. If it becomes worse, I can always revert back to local storage just for one app.
