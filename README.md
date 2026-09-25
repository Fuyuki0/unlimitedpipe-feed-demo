# UnlimitedPipe feeds

26 free feeds, updated every hour by a GitHub Actions workflow and served by GitHub Pages.
No server, no database, no account. Each feed is one short YAML file, built with
[UnlimitedPipe](https://pypi.org/project/unlimitedpipe/).

**Browse and subscribe: https://fuyuki0.github.io/unlimitedpipe-feeds/**

Paste any `.xml` link into a feed reader. Every feed also exists as a JSON Feed (same name,
`.json`) that carries full UnlimitedPipe events with provenance, so other pipelines can build
on it: `unlimited rss https://fuyuki0.github.io/unlimitedpipe-feeds/ai-news.json`.

### AI

| Feed | What it follows |
| --- | --- |
| [ai-news](https://fuyuki0.github.io/unlimitedpipe-feeds/ai-news.xml) | AI and LLM stories from Hacker News and Lobsters |
| [ai-labs](https://fuyuki0.github.io/unlimitedpipe-feeds/ai-labs.xml) | OpenAI, Google DeepMind and Hugging Face announcements |
| [ai-papers](https://fuyuki0.github.io/unlimitedpipe-feeds/ai-papers.xml) | Hugging Face Daily Papers: the research the community highlights each day |
| [arxiv-llm](https://fuyuki0.github.io/unlimitedpipe-feeds/arxiv-llm.xml) | New arXiv papers on language models and agents |
| [ai-releases](https://fuyuki0.github.io/unlimitedpipe-feeds/ai-releases.xml) | Releases of Ollama, llama.cpp, vLLM, Transformers, LangChain, ComfyUI, Open WebUI |

### Developers

| Feed | What it follows |
| --- | --- |
| [dev-releases](https://fuyuki0.github.io/unlimitedpipe-feeds/dev-releases.xml) | Releases of uv, Ruff, Node.js, Deno, Bun, VS Code, Rust, TypeScript |
| [cloud-status](https://fuyuki0.github.io/unlimitedpipe-feeds/cloud-status.xml) | New incidents at GitHub, Cloudflare, OpenAI, Anthropic and Google Cloud |
| [hn-top](https://fuyuki0.github.io/unlimitedpipe-feeds/hn-top.xml) | Hacker News stories with 300+ points |
| [show-hn](https://fuyuki0.github.io/unlimitedpipe-feeds/show-hn.xml) | Show HN projects with 100+ points |
| [python-news](https://fuyuki0.github.io/unlimitedpipe-feeds/python-news.xml) | Python releases and new PEPs |
| [rust-news](https://fuyuki0.github.io/unlimitedpipe-feeds/rust-news.xml) | The official Rust blog |

### Security

| Feed | What it follows |
| --- | --- |
| [exploited-vulnerabilities](https://fuyuki0.github.io/unlimitedpipe-feeds/exploited-vulnerabilities.xml) | Vulnerabilities newly added to CISA's Known Exploited list |
| [security-news](https://fuyuki0.github.io/unlimitedpipe-feeds/security-news.xml) | Krebs on Security, BleepingComputer, The Hacker News, Schneier on Security |
| [sec-cyber-incidents](https://fuyuki0.github.io/unlimitedpipe-feeds/sec-cyber-incidents.xml) | Public companies disclosing a material cybersecurity incident to the SEC (8-K Item 1.05) |

### Money and government

| Feed | What it follows |
| --- | --- |
| [sec-company-events](https://fuyuki0.github.io/unlimitedpipe-feeds/sec-company-events.xml) | Bankruptcies, completed acquisitions, layoffs, delistings, auditor changes and restatements from SEC 8-K filings |
| [sec-ipo-filings](https://fuyuki0.github.io/unlimitedpipe-feeds/sec-ipo-filings.xml) | Companies filing to go public in the US (SEC S-1 and F-1) |
| [lobbying-big-spenders](https://fuyuki0.github.io/unlimitedpipe-feeds/lobbying-big-spenders.xml) | US lobbying reports of $1 million or more, as filed with Congress |
| [sanctions-actions](https://fuyuki0.github.io/unlimitedpipe-feeds/sanctions-actions.xml) | New US sanctions actions from the Treasury (OFAC): designations, removals, licenses |
| [us-new-rules](https://fuyuki0.github.io/unlimitedpipe-feeds/us-new-rules.xml) | Significant new US federal rules from the Federal Register |

### News

| Feed | What it follows |
| --- | --- |
| [world-headlines](https://fuyuki0.github.io/unlimitedpipe-feeds/world-headlines.xml) | BBC, NPR and Al Jazeera headlines, merged |
| [climate-news](https://fuyuki0.github.io/unlimitedpipe-feeds/climate-news.xml) | Climate and energy stories |
| [thailand-news](https://fuyuki0.github.io/unlimitedpipe-feeds/thailand-news.xml) | Thailand news in English (Khaosod English, Thai Enquirer) |
| [crypto-news](https://fuyuki0.github.io/unlimitedpipe-feeds/crypto-news.xml) | CoinDesk, Cointelegraph and Decrypt, merged |

### Science and space

| Feed | What it follows |
| --- | --- |
| [earthquakes](https://fuyuki0.github.io/unlimitedpipe-feeds/earthquakes.xml) | Significant earthquakes worldwide (USGS) |
| [space-launches](https://fuyuki0.github.io/unlimitedpipe-feeds/space-launches.xml) | Rocket launches worldwide as soon as they are scheduled (Launch Library 2) |
| [nasa-image](https://fuyuki0.github.io/unlimitedpipe-feeds/nasa-image.xml) | NASA Image of the Day |

## How it works

Each file in [`feeds/`](feeds) is a complete pipeline: where to read, what to keep, where to
write. For example, [`feeds/exploited-vulnerabilities.yml`](feeds/exploited-vulnerabilities.yml)
reads CISA's official JSON, builds a title and an NVD link for each vulnerability, and emits
only the ones it has not seen before.

[`.github/workflows/unlimitedpipe-feeds.yml`](.github/workflows/unlimitedpipe-feeds.yml) was
generated by `unlimited publish feeds/*.yml` and runs them all every hour. What each feed has
already seen lives in `.unlimitedpipe/state/`, so every run adds only new items. A source that
is down keeps its feed as it was; the other feeds still update.

Sources are official feeds and APIs, read politely: robots.txt respected, one request per
second per site, conditional requests. Items link to the original articles; titles and short
summaries come from the sources' own feeds.

## Make your own

1. Fork this repository and delete the feeds you don't want.
2. Add yours: `pip install unlimitedpipe`, then `unlimited new https://some-site.example`
   writes a starting pipeline, or copy one from `feeds/`.
3. Run `unlimited publish feeds/*.yml --force` to regenerate the workflow and index page.
4. In your fork's Settings, enable Actions and set Pages to deploy from GitHub Actions.

## Suggest a feed

Open an issue with a source (an RSS feed, an official API or a public page) and what to follow
in it.
