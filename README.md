# Codex web: using the Codex coding agent from your browser

*Unofficial community guide for Codex web. Not affiliated with OpenAI. All trademarks belong to their owners.*

This is a working guide to Codex web, the browser-hosted version of the Codex coding agent that runs inside ChatGPT. It covers what the cloud surface is, how it relates to the Codex desktop app, CLI and IDE integrations, what the plan situation looks like as of the sources linked below, and the gotchas that trip people up when they move from a local agent to a hosted one. Everything factual here is taken from the pages listed at the end; where a detail is not on those pages, I say so rather than guess.

> Only need a landing page or a small app, not a whole repository workflow? [Try Begin.sh - turn a prompt or a URL into a downloadable static site or Expo app](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=codex-web&utm_content=readme-top&utm_term=tier-r). It gives you a zip you host yourself, with no backend or auth to manage.

## What it is

Codex is OpenAI's coding agent. The cloud page describes it as "the same powerful coding agent, now in ChatGPT": you log in to ChatGPT, open the Codex section, and hand off engineering work that the agent carries out on your behalf. The marketing copy positions it for "real engineering work", from routine pull requests upward, and the same page lists Heidi, NVIDIA, Cisco and Shopify as teams using it.

The web surface is one of four places you can run Codex. According to the February 2026 announcement of the Codex app for macOS (Windows followed on March 4, 2026), Codex runs in the app, from the CLI, in your IDE, and in the cloud, and one set of rate limits applies across all of them. The app post also frames how the product has evolved since the April 2025 launch: models now handle long-running tasks end to end, so the emphasis has moved to orchestrating multiple agents, delegating work and running tasks in parallel. The web version is the entry point that needs nothing installed.

## How to get started

1. Open the Codex cloud page at [chatgpt.com/codex/cloud](https://chatgpt.com/codex/cloud) and sign in with your ChatGPT account. The page redirects through the normal ChatGPT login.
2. Check which plan you are on. The plan pages are linked from the ChatGPT pricing menu: [Free](https://chatgpt.com/plans/free/), [Go](https://chatgpt.com/plans/go/), [Plus](https://chatgpt.com/plans/plus/), [Pro](https://chatgpt.com/plans/pro/), [Business](https://chatgpt.com/business/) and [Enterprise](https://chatgpt.com/business/enterprise/).
3. Read the [Codex overview](https://chatgpt.com/codex/) and the [developer docs](https://developers.openai.com/codex/) before your first task. The docs are the authoritative reference for connecting repositories and configuring the agent.
4. If you want a local surface as well, the [ChatGPT download page](https://chatgpt.com/download/) is where the desktop app lives. The app post describes it as a command center for running several agents at once.
5. Start with a small, well-scoped task (a single bug, a single test file) so you can judge the output before delegating anything larger.

## Pricing and limits

The app announcement says that, for a limited time, Codex is included with ChatGPT Free and Go, and that rate limits were doubled on Plus, Pro, Business, Enterprise and Edu plans. Those limits apply everywhere Codex runs, including the web. The announcement does not give the numbers, and "limited time" has no end date on the page, so check the [Codex pricing page](https://chatgpt.com/codex/pricing/) for current rates and quotas. Enterprise terms are on the [Codex enterprise page](https://chatgpt.com/codex/enterprise/).

## Practical notes and gotchas

- One rate-limit pool. Because limits are shared across app, CLI, IDE and cloud, a heavy session in the desktop app eats into what you can do on the web the same day. Plan long parallel runs accordingly.
- Cloud tasks are asynchronous by design. The app post describes agents that take on work spanning hours, days or weeks. Write the task description as if for a colleague who cannot ask follow-up questions: state the goal, the constraints and how to verify success.
- Parallel agents multiply review load, not just throughput. Running several tasks at once is the headline feature of the app; the bottleneck becomes your ability to review what comes back.
- Skills and Automations are app concepts. Whether each is available on the web surface is not stated on the pages I used, so verify in the developer docs.
- Security defaults are described as "secure by default, configurable by design". Read that section of the app post before granting an agent access to anything sensitive.
- The Free and Go inclusion is explicitly temporary, so do not build a team process on it without checking the pricing page.

## Comparison

| | Codex web | Codex app (macOS, Windows) | Begin.sh |
|---|---|---|---|
| Where it runs | In the browser, inside ChatGPT | Installed desktop app | In the browser |
| Typical output | Code changes and pull requests in your repositories | Same, with multiple agents managed in parallel | A zip containing a static site or an Expo app |
| Install required | No | Yes | No |
| Hosting or backend included | Not applicable | Not applicable | None; you download and host the result yourself |
| Rate limits | Shared with app, CLI and IDE | Shared with web, CLI and IDE | Check the site |

## FAQ

**Is Codex web the same agent as the desktop app?**
The cloud page says it is the same coding agent, delivered inside ChatGPT. The app adds a local interface for supervising several agents at once.

**Do I need a paid ChatGPT plan?**
At the time of the app announcement, Codex was included with Free and Go for a limited time. Paid plans received doubled limits. Check the pricing page for the current state.

**Do rate limits differ between the web and the CLI?**
No. The announcement says the higher limits apply everywhere you use Codex.

**Where is the technical documentation?**
The developer docs at developers.openai.com/codex are linked from the Codex menu on chatgpt.com. OpenAI also lists Codex events on its academy site.

**Can I run more than one task at a time?**
Running work in parallel is the central theme of the app announcement. How many concurrent cloud tasks your plan allows is not stated on the pages used here.

## When a full coding agent is more than you need

Codex web is built for repositories: pull requests, refactors, test suites. A lot of requests that reach a coding agent are smaller than that, for example a marketing page, a one-off microsite, or a mobile prototype to show a client. For those, a generator that outputs a finished artifact can be faster than steering an agent through a repo. [Try Begin.sh - turn a prompt or a URL into a downloadable static site or Expo app](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=codex-web&utm_content=readme-top&utm_term=tier-r). You describe the page or paste a URL to clone, download the zip, and host it wherever you like. There is no hosting, backend or auth layer bundled in, which is exactly the point for throwaway or static projects.

## Sources

- Codex cloud page: chatgpt.com/codex/cloud
- Introducing the Codex app (OpenAI, February 2, 2026, updated March 4, 2026): openai.com/index/introducing-the-codex-app
- Getting started with Codex (Dometrain blog): dometrain.com/blog/getting-started-with-codex


_Last reviewed: 2026-09-22_
