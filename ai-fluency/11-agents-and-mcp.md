# Agent Concepts and MCP Basics (FL-05)

**Agent** = a model that plans, calls tools, reads the results and decides the next step until a goal is done.
**MCP (Model Context Protocol)** = a standard plug that lets the model use outside tools (GitHub, Calendar, Gmail,
browser) through one interface, with permissions controlled by me.

**One working setup — three real tool-call tasks from my internship (Claude with connectors):**
1. **GitHub:** cloned my internship repo, ran and executed notebooks, compared my uploaded files with the local versions.
2. **Browser (Claude in Chrome):** opened the FlyRank portal, filled and saved assignment submissions, enabled GitHub Pages.
3. **Google Calendar:** created my recurring "add next case study" reminder —
   https://calendar.google.com/calendar/event?eid=anJycmJzbXZmbXM2MjVzNDJrMzR2OW92ZmsgZm91bmRlcnM3ODZAbQ

**Where a human must stay in the loop:** sign-ins, file uploads, repo settings, anything public — the agent asked me first.
