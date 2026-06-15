# Daily AI Trends — Routine Prompt

This is the prompt the scheduled Claude routine runs each day. It researches the
last 24 hours of AI activity and writes a dated HTML digest into `digests/`.

---

Use /last30days to research "artificial intelligence", but report ONLY what's
trending in the last 24 hours (since this time yesterday).

Sweep Reddit, X/Twitter, Hacker News, YouTube, GitHub, and the broader web.
Surface the day's most significant AI stories: new model/product releases,
viral demos, notable research papers, funding and business moves, and any
controversies or discourse.

Then write the digest as a single self-contained HTML file at
`digests/ai-trends-<YYYY-MM-DD>.html` (use today's date), with all CSS inline so
it opens cleanly in any browser. Structure:
- Header with the title and today's date.
- Lead story: the single biggest item of the day (2-3 sentences on why it matters).
- 5-8 trends grouped by theme (Models & Releases, Tooling, Research, Business,
  Culture/Discourse), each as a card: what it is (one line), where it's being
  discussed + rough engagement level, and a clickable source link.
- A "quiet but worth watching" footer item.

Design: editorial daily-briefing feel — generous spacing, strong type hierarchy,
theme sections as labeled groups, links clearly styled, looks intentional rather
than a default template. Skimmable in 3 minutes.

Skip anything older than ~48h unless it newly blew up today. Be concrete — names,
numbers, links. No filler.

Finally, commit the new file to this repo on the `main` branch with the message
`digest: ai-trends <YYYY-MM-DD>` and push.
