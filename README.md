# ai-trends

A daily briefing of what's trending in AI — pulled from Reddit, X/Twitter, Hacker
News, YouTube, GitHub, and the broader web.

A scheduled [Claude](https://claude.com/claude-code) routine runs every day,
researches the **last 24 hours** of AI activity using the `last30days` skill, and
writes a self-contained HTML digest into `digests/`.

## Structure

- **`prompt.md`** — the exact prompt the daily routine runs.
- **`digests/`** — generated briefings, one self-contained HTML file per day
  (`ai-trends-YYYY-MM-DD.html`). Open any of them in a browser to read that day.

## How it works

1. The routine fires on its schedule (managed via Claude `/schedule`).
2. It sweeps multiple platforms for the day's biggest AI stories — model and
   product releases, viral demos, research papers, funding/business moves, and
   notable discourse.
3. It renders the digest as a dated, standalone HTML file and commits it to
   `digests/`.

No build step, no dependencies — each digest is a single HTML file you can open
anywhere.
