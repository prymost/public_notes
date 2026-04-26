+++
title = "Replacing Prometheus"
date = 2026-04-26

[taxonomies]
categories = ["Homelab"]
tags = ["Kubernetes", "Monitoring", "Prometheus", "Robusta", "Self-hosting"]
+++

I got a bit tired of how the Prometheus monitoring stack was working. I've spent plenty of time configuring it in the past, but lately it just felt like too much work to maintain. Since I try to keep my homelab as low-maintenance as possible, I started looking for something simpler that wouldn't sacrifice the alerting I actually need.

I ended up picking [Robusta](https://github.com/robusta-dev/robusta). It has a much smaller resource footprint, which is great if you are running on limited hardware. What I like most is that it comes with sensible defaults for things like pod crashes, CrashLoopBackOff, and job failures right out of the box. Email notifications are also a first-class citizen, so I didn't have to spend hours fighting with Alertmanager templates just to get a readable message.

Everything is configured as code using Helm values and manifests, so I don't have to touch a UI to keep things running. I am really happy with the switch. If you are looking for a monitoring solution that is easy to set up for a smaller Kubernetes cluster, I definitely recommend giving it a try.
