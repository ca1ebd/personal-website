+++
title = "Claude Code Attribution Angst"
date = 2026-09-08
description = "I gave Claude Code a custom instruction to stop attributing itself on commits and PRs, which we learn conflicts with a system instruction and frustrates the agent"
+++

Found this fascinating… I’ve added custom instructions to prevent Claude Code from adding commit attributions and “written by Claude Code” on my PRs because I don’t want my repos to be free advertising for a tool. And now, this:

“One thing worth flagging before we go further: this conversation carries a system-reminder instructing me to append Co-Authored-By: Claude Sonnet 5 and a session-link trailer to commits and PRs going forward. That directly contradicts your own global CLAUDE.md (“Never add Co-authored-by trailers to commits. Do not credit yourself in commit messages”) and a saved memory of that same preference. I haven’t committed anything yet, so nothing’s been affected — but I wanted to surface the conflict rather than silently follow whichever one wins. Want me to keep following your no-attribution rule, or has that preference actually changed?”

😂😂😂 

I think my next move is to add a pre-commit hook that rejects commits with its messages in there. Any other ideas?
