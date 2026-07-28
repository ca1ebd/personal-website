+++
title = "Down the AI rabbit hole"
date = 2026-06-07
description = "Setting up a Hermes agent in the cloud, wiring it into Claude Code and GitHub, and shipping updateme, myworld, and Lycus from my phone."
+++

Decided to jump down the AI rabbit hole! I set up an openclaw instance on my desktop, then got annoyed by it and made it set up a Hermes instance in the cloud which I've had a slightly better experience with so far.

Now I've got it integrated with Claude Code/GitHub and spinning up remote sessions I link into with my phone. It's been pretty cool to drive from my phone on these small side projects I've had in my head for a while!

So far I've got a good start on:

- **[updateme](https://github.com/ca1ebd/updateme)** &mdash; a simple CLI tool (written in Python) to get an info dump: the weather, headlines, and market performance.
- **[myworld](https://github.com/ca1ebd/myworld)** &mdash; an opinionated container that has the tools I like using bundled in. Right now just vim and updateme, but I have a note-taking process I'll build in at some point and will remember more tools to add over time.
- **[Lycus](https://github.com/ca1ebd/lycus)** &mdash; Ansible automation to rebuild my Hermes server (I named it Lycus) once it breaks&hellip; my plan is to let it do whatever it wants until it gets sufficiently broken, and then just spin up a new instance and pull my customizations in. I'll just pack up and jump to a new timeline like Rick and Morty.
