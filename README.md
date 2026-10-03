# Searcherries for Claude

All your GEO and SEO data in Claude, with workflows that turn it into page changes.

[Searcherries](https://searcherries.com) tracks how AI assistants answer the questions your customers ask, which brands and sources those answers name, and what your Google Search Console, Bing Webmaster Tools and GA4 AI-traffic data says. This plugin connects Claude to that data and adds ready-made workflows for GEO work. It works in Claude chat, in Cowork and in Claude Code; in Claude Code the workflows can end with edits to your website's code, shown to you before they are applied.

## What's included

| Component | What it does |
|-----------|--------------|
| Connector `searcherries` | The Searcherries MCP server at `https://app.searcherries.com/mcp/searcherries`: read-only, OAuth sign-in, nine tools for AI visibility, competitors, citations, Search Console, Bing and GA4 data |
| `/searcherries:action-plan` | Your next five priorities with dated evidence, an owner and a success measure (`project`, `audience`, `period`) |
| `/searcherries:geo-audit` | Visibility score and change, where the brand is invisible, who wins, which sources shape the answers, five actions (`project`, `period`) |
| `/searcherries:content-gaps` | Pages to publish or update, with the demand that proves each one (`project`, `topic`) |
| `/searcherries:competitor-gap` | One competitor: the questions it wins, what it is praised for, the pages that cite it, a counter-content plan (`competitor`, `project`) |
| `/searcherries:page-brief` | A brief for one page: queries and AI questions to answer, citation competition, sections and facts (`url`, `project`, `question`) |
| `/searcherries:question-review` | Which tracked questions to keep, rephrase, retire or add (`project`) |
| `/searcherries:weekly-report` | One-page status with deltas, trends, competitor moves and three actions (`project`, `period`) |
| Skill `improve-ai-visibility` | Applied automatically when you ask why AI assistants leave your brand out or what to change on your site: gaps, competitors, citations, search demand, then page changes |

Every workflow reads data through the connector only. Nothing in this plugin runs scripts, stores data or sends data anywhere other than the Searcherries server you sign in to.

## Requirements

A Searcherries account on a paid plan (an active trial counts) with at least one project. [Start here](https://app.searcherries.com/register).

## Install and connect

From the directory: add **Searcherries** in Claude under Customize → Plugins, then connect the Searcherries connector on the plugin's Connectors tab and approve access in your browser. The plugin also loads in your Claude Code sessions.

From this repository, in Claude Code:

```sh
claude plugin marketplace add eduardmur/searcherries-claude-plugin
claude plugin install searcherries@searcherries
```

Then run `/mcp`, choose `searcherries` and sign in to Searcherries in the browser.

## Try it

- `/searcherries:action-plan` — "What should I work on next?"
- `/searcherries:competitor-gap Acme` — why Acme is recommended instead of you and how to catch up
- "Which of our pages should we update first to get recommended by AI assistants? Show the evidence." — runs the `improve-ai-visibility` skill

Every number comes with the period it was measured in. The connector is read-only: it cannot change projects, questions or billing, and it only sees the projects of the account you authorize. Tool reference: [searcherries.com/docs/mcp/tools](https://searcherries.com/docs/mcp/tools).

## Support

[Open an issue](https://github.com/eduardmur/searcherries-claude-plugin/issues) or write from your account at [app.searcherries.com](https://app.searcherries.com).

## License

MIT
