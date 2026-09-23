+++
title = "Claude Code Attribution Victory"
date = 2026-09-22
description = "I win this battle in the war against agents trying to advertise on my projects via git pre-commit hooks"
+++

Claude Code, conceding defeat in our battle over attributions twice this week:

“A local `commit-msg` hook blocks Claude attribution lines — your `claude-attribution-guard` at work. Your hook wins over my default attribution instruction, so dropping the line.”

“One note: the repo's commit-msg hook rejects the `Co-Authored-By` / `Claude-Session` lines my session instructions ask for, so I committed without them.”

I enjoy using Claude Code, but I don't want my repos turning into free advertising for it. By default it adds itself as a co-author on commits and PRs. The audacity! It’s the new version of “Sent from my iPhone”

My first attempt was a competing instruction in my project config. The result was a [recurring agent mental breakdown](@/blog/claude-code-attribution-angst.md) over the conflicting system instruction: wasted tokens, more hallucination (competing instructions invite it), and it only worked about half the time. Check out my last post for the session quote.

Version two is a git `commit-msg` hook that rejects any commit matching the attribution lines. Unlike a settings toggle, it's enforced by git itself, so it holds regardless of tool, version, or who's committing. I've run it across dozens of sessions with zero leaks. And I get to watch the agent graciously admit defeat, which is quite satisfying.

The bigger lesson: no matter how much all caps and asterisks you use, instructions to an AI are only ever suggestions. If your agent isn't sticking to your standards, find a place to add a deterministic check.

Want to [take back the power over your own project](https://github.com/ca1ebd/agent-attribution-blocker)?
