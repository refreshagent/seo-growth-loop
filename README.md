# SEO Growth Loop

[![Skills](https://skills.sh/b/refreshagent/seo-growth-loop)](https://skills.sh)

An agent skill that runs a closed-loop SEO growth workflow using Search Console performance data, keyword demand analysis, SERP Authority Mark checks, and whatever publishing path the project exposes.

## Usage

```bash
npx skills add refreshagent/seo-growth-loop
```

Or for a specific agent:

```bash
npx skills add refreshagent/seo-growth-loop -a opencode -a claude-code
```

## What it does

The skill implements a recursive decision loop:

1. **Gather performance** from GSC, Bing, or analytics
2. **Check memory** — read existing logs, topical maps, sitemaps
3. **Optimize before building** — prefer improving existing URLs with real impressions
4. **Validate demand** with keyword data
5. **Run Authority Mark** for net-new targets
6. **Choose one action** justified by evidence
7. **Publish** through the project's available adapter
8. **Verify** the rendered output
9. **Submit for indexing**
10. **Log the baseline and change**

It adapts to CMS/API, local repo, hybrid, or advisory-only environments.

## Structure

```
seo-growth-loop/
├── SKILL.md              # Entry point — agent loads this
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml       # OpenAI GPT metadata
└── references/
    ├── agent-runtimes.md
    ├── log-template.md
    ├── project-config.md
    ├── publishing-adapters.md
    └── scheduling.md
```
