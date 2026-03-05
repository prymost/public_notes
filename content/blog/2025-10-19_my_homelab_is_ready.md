+++
title = "My Homelab is Ready!"
date = 2025-10-19

[taxonomies]
categories = ["Homelab"]
tags = ["Kubernetes", "K3s", "FluxCD", "GitOps", "Monitoring", "Prometheus", "Grafana", "Debian"]
+++

I'm very happy to share that I've finished setting up my **homelab**!

It took about a month to go from "I want to run a homelab on **Kubernetes**" to successfully using my first self-hosted app. I thought it would take much longer with my limited time, so this is a big personal milestone.

I have two **old laptops** I got from friends sitting in my garage, running a Kubernetes cluster leveraging **Debian** and **k3s**. At the moment, it's a full monitoring stack (**Prometheus** + **Grafana**) and a simple app, all running smoothly. Seeing the metrics in Grafana for the first time was incredibly satisfying.

This entire setup relies on a **GitOps** flow, specifically using **FluxCD** to manage all deployments. I had to fight a number of quirks setting everything up, obviously, but that's just a part of the learning process.

Next up: adding some security layers, then deploying more useful applications.

If you want the technical details, check out my [Homelab repository](https://github.com/prymost/homelab) on GitHub.
