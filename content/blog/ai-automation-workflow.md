+++
title = "AI-enabled development workflow for infrastructure and automation"
date = 2026-07-28
description = ""
draft = true
+++

This past week I decided to set up some monitoring for a family member's small business that I support. What I deployed isn't all that interesting, an open source monitoring solution (Uptime Kuma) that is able to monitor the business website, email servers, VPN, NAS, etc. But this project has allowed me to validate a new process I've been working on to best leverage AI tools for cloud infrastructure work:

1. Detailed spec first.

Before provisioning anything, I iterated with AI tools to generate a detailed spec which laid out the stack, tools and design choices up front. We're deploying Uptime Kuma on an Azure VM with x SKU, running Ubuntu. And then detailing network access, authn/authz, etc.

2. First pass deployment.

Had the AI provision a fresh VM and implement that spec one step at a time. Every place reality diverged from the spec — a bug in my own spec, a platform quirk, a security tradeoff worth reconsidering — got captured live in a running changes doc, with the reasoning behind it. Then reconciled that back into the spec so it included the new learnings.

3. A second spec, for the automation itself.

Once the first pass deployment was was functional and met the spec, I had it write a new spec — this time for automating the whole thing with Terraform + Ansible.

4. Build automation, validate with a second instance.

Implemented that spec, then directed the AI tools to run the automation to stand up a second, fully isolated instance and compare it against the original.

5. Iterate until it's a precise replica.

Found real bugs this way — the kind a human following the spec alone would probably also hit. Each one went back into the changes doc and got fixed in the automation itself, not patched around.

6. Cut over.

Once the automated deployment was a verified, precise replica of the hand-built one, we swapped it in for the real thing. I kept the original around as a rollback option until I could verify, and then deleted it.

I'm happy with this process because I want automation to boot, but starting with automation tools adds another layer to trudge through when validating and testing the core idea. It also models how I would approach automation work pre-AI, it just leverages AI to do the boring stuff and allows me to focus on the more interesting tradeoffs and design questions.

I also did ~96% of the work from my phone in anywhere from 5-30 minute sessions while riding in the car or in between chores/activities for the day...

Anyone else have learnings on using AI for DevOps/Automation/Infrastructure work?