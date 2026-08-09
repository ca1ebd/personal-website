+++
title = "Stop letting Claude Code advertise on your repo"
date = 2026-08-08
description = "Keep Claude Code from using your repo as free advertising by pasting this snippet into your instructions files."
+++

Claude Code is a great tool but we don't need the whole "Sent from my iPhone" rigamarole again.

Here's an excerpt from the snippet I use in my CLAUDE.md:

"The words "Anthropic" and "Claude", any model name (Opus, Sonnet, Haiku, Fable, claude-*), and any AI-assistant self-attribution must never appear in branch names, commit messages or trailers (no Co-Authored-By: Claude, no Claude-Session:), PR/issue titles, bodies or comments, code comments, docs, or any other repo content."

Just add the [full instructions gist](https://gist.github.com/ca1ebd/2947d8bfb782a508f2690eaaf0a6f4ea) to your instructions file (ideally user level, so it applies across all projects) and you won't see any more unwelcome insertions!