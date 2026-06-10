+++
title = "daily summary ai skill"
date = 2026-06-10

[taxonomies]
categories = ["Productivity"]
tags = ["AI", "Automation", "Note-taking", "Claude Code", "Journaling", "GitHub"]
+++


For years I've been writing down what I worked on each day. Partly to look back and remember things, partly as a running record for performance reviews or when someone asks "how did you do that thing six months ago?" It works for both work and personal projects.

The problem is that I don't actually enjoy the writing part. I'd sometimes do it mid-day, sometimes in the evening trying to reconstruct what I'd done, sometimes the next morning looking back at the day before. The most valuable part is always the looking back, not the writing itself.

So I started using AI for this. I created a Claude Code skill that runs at the end of the day and automatically collects what I've done: coding agent logs, GitHub activity, Jira issues assigned to me, Slack threads I participated in, and my calendar. From all of that it generates a concise summary with embedded links, which then gets written directly into my journal.

The part I find most useful is that it also posts comments back to the relevant Jira tickets. That means my teammates can see what happened on a ticket without me writing it up separately, and six months later I can look at any ticket and see exactly what was done and why.

For personal projects the setup is simpler, just coding logs without the work integrations, but it's still useful.

I'm not sharing the exact skill text because I think the point is for each person to customize it for what matters to them, not copy what matters to me. But if you have a habit of writing things down, or want to build one with the goal of being able to recall how something was done or why a decision was made, this kind of skill makes the entry into that workflow almost effortless.