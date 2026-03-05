+++
title = "Debugging K8s Network Policies"
date = 2025-11-02

[taxonomies]
categories = ["DevOps"]
tags = ["Kubernetes", "K8s", "Network Policies", "Security", "Debugging", "Networking"]
+++

My focus last week (in personal projects space) was to add network policies to my **homelab**. I added them to all custom namespaces but, in the end, had to revert some and replace them with less restrictive ones because some things just stopped working, and I had no time to investigate why.

The biggest challenge was in the very beginning when none of the policies I added did anything. Everything looked good in the logs and on the **K8s** cluster. I mean, there were no errors or reports of invalid configs.

After several hours of cumulative debugging, checking all configs, and brainstorming with AI, I found that my nodes just didn't have the **iptables** binary! 🤦

Everything looked great in the logs, but no rules were enforced. After adding the binary and updating my bootstrap scripts, all the rules started working as intended.
