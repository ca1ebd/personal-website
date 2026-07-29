+++
title = "Launching my personal website"
date = 2026-07-28
description = "Staking out my claim on the internet: launching a personal website."
+++

I'm excited to finally launch a personal website instead of just pointing people at LinkedIn. 


I've heard an optimistic vision for the AI future - everybody is able to self-host open source tools and build their own software to get free of big tech control. So I guess this is me doing my part (wink)


Built it the same way as the last few side projects: primarily driving Claude Code running on my project VPS from my phone. Bio, work history, a projects page linking out to the other things I've been building.


Here's what's running under the hood:


* Blog: running on [Zola](https://www.getzola.org/), a Rust-based static site generator. I write a post in markdown, it renders to plain HTML at build time.
* CI/CD: same pattern as the contraction timer — merge to main deploys prod, push to any other branch deploys to a test environment automatically. Two separate Azure Static Web Apps, one shared GitHub Actions. This works well for my workflow to collaborate with AI. 
* Link previews: I've added Open Graph tags so sharing the link doesn't just show bare text. I'd always wondered how those link previews worked... now I know. I even found a cool tool that will show you what they look like on different platforms: [opengraph.xyz](https://www.opengraph.xyz/url/https%3A%2F%2Fcalebdudley.dev)


It's nothing crazy, but it feels to good to have a platform for sharing that I control.


Check it out: https://calebdudley.dev 


Any bugs I missed? Or SEO advice so it shows up when someone searches me?