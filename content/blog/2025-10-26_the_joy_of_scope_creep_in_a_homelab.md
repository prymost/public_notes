+++
title = "The Joy of Scope Creep in a Homelab"
date = 2025-10-26

[taxonomies]
categories = ["Homelab"]
tags = ["Security", "Kubernetes", "K8s", "Automation", "Learning", "Project Management"]
+++

Last week was a classic case of **scope creep** (for a personal project): I started one task and it instantly spawned five more. On one hand, it's a good learning process; on the other, it feels less productive because my To-Do list got bigger, not smaller.

All I wanted was to set up some **security scanner** for my **homelab K8s cluster**. After researching different tools, I spun one up and got a summary report, which was great. Time to start fixing vulnerabilities and misconfigurations, right?

Well, I thought I needed to set up alerting first so I know the number does not go up. But for that, I need to set up **secret management** so alerts can be sent via email. And each part requires quite a bit of reading, research, and evaluation of which solution will work best for my case.

And so, by the end of the week, my To-Do list for the homelab is twice as big as it was when the week started. And I love it. I am learning so much with this project.
