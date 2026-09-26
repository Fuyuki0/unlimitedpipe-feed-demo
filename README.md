# UnlimitedPipe feeds

50 free feeds, updated every hour by a GitHub Actions workflow and served by GitHub Pages.
No server, no database, no account. Each feed is one short YAML file, built with
[UnlimitedPipe](https://pypi.org/project/unlimitedpipe/).

**Browse and subscribe: https://feeds.daemonfill.dev/**

Paste any `.xml` link into a feed reader. Every feed also exists as a JSON Feed (same name,
`.json`) that carries full UnlimitedPipe events with provenance, so other pipelines can build
on it: `unlimited rss https://feeds.daemonfill.dev/ai-news.json`.

### AI

| Feed | What it follows |
| --- | --- |
| [ai-news](https://feeds.daemonfill.dev/ai-news.xml) | AI and LLM stories from Hacker News and Lobsters |
| [ai-labs](https://feeds.daemonfill.dev/ai-labs.xml) | OpenAI, Google DeepMind and Hugging Face announcements |
| [ai-papers](https://feeds.daemonfill.dev/ai-papers.xml) | Hugging Face Daily Papers: the research the community highlights each day |
| [arxiv-llm](https://feeds.daemonfill.dev/arxiv-llm.xml) | New arXiv papers on language models and agents |
| [ai-releases](https://feeds.daemonfill.dev/ai-releases.xml) | Releases of Ollama, llama.cpp, vLLM, Transformers, LangChain, ComfyUI, Open WebUI |

### Developers

| Feed | What it follows |
| --- | --- |
| [dev-releases](https://feeds.daemonfill.dev/dev-releases.xml) | Releases of uv, Ruff, Node.js, Deno, Bun, VS Code, Rust, TypeScript |
| [cloud-status](https://feeds.daemonfill.dev/cloud-status.xml) | New incidents at GitHub, Cloudflare, OpenAI, Anthropic and Google Cloud |
| [hn-top](https://feeds.daemonfill.dev/hn-top.xml) | Hacker News stories with 300+ points |
| [show-hn](https://feeds.daemonfill.dev/show-hn.xml) | Show HN projects with 100+ points |
| [python-news](https://feeds.daemonfill.dev/python-news.xml) | Python releases and new PEPs |
| [rust-news](https://feeds.daemonfill.dev/rust-news.xml) | The official Rust blog |

### Security

| Feed | What it follows |
| --- | --- |
| [exploited-vulnerabilities](https://feeds.daemonfill.dev/exploited-vulnerabilities.xml) | Vulnerabilities newly added to CISA's Known Exploited list |
| [security-news](https://feeds.daemonfill.dev/security-news.xml) | Krebs on Security, BleepingComputer, The Hacker News, Schneier on Security |
| [security-advisories](https://feeds.daemonfill.dev/security-advisories.xml) | Critical advisories and alerts from CERT-EU, JPCERT/CC (Japan) and the Canadian Centre for Cyber Security |
| [data-breaches](https://feeds.daemonfill.dev/data-breaches.xml) | Data breaches added to Have I Been Pwned, with accounts and data exposed (CC BY 4.0) |
| [sec-cyber-incidents](https://feeds.daemonfill.dev/sec-cyber-incidents.xml) | Public companies disclosing a material cybersecurity incident to the SEC (8-K Item 1.05) |

### Money, economy and government

| Feed | What it follows |
| --- | --- |
| [sec-company-events](https://feeds.daemonfill.dev/sec-company-events.xml) | Bankruptcies, completed acquisitions, layoffs, delistings, auditor changes and restatements from SEC 8-K filings |
| [sec-ipo-filings](https://feeds.daemonfill.dev/sec-ipo-filings.xml) | Companies filing to go public in the US (SEC S-1 and F-1) |
| [lobbying-big-spenders](https://feeds.daemonfill.dev/lobbying-big-spenders.xml) | US lobbying reports of $1 million or more, as filed with Congress |
| [sanctions-actions](https://feeds.daemonfill.dev/sanctions-actions.xml) | New US sanctions actions from the Treasury (OFAC): designations, removals, licenses |
| [us-new-rules](https://feeds.daemonfill.dev/us-new-rules.xml) | Significant new US federal rules from the Federal Register |
| [central-banks](https://feeds.daemonfill.dev/central-banks.xml) | Press releases of the Fed, ECB, Bank of Japan, Bank of England and Reserve Bank of India, without routine operations |
| [world-leaders](https://feeds.daemonfill.dev/world-leaders.xml) | Official announcements of the White House, the Kremlin and the European Commission |
| [usd-rates](https://feeds.daemonfill.dev/usd-rates.xml) | The US dollar against the baht, yen, yuan, rupee and euro, daily (ECB reference rates) |

### Crypto

Data, not investment advice.

| Feed | What it follows |
| --- | --- |
| [exchange-listings](https://feeds.daemonfill.dev/exchange-listings.xml) | New and removed trading pairs on Coinbase, Binance, OKX and Upbit, from each exchange's official market list |
| [crypto-hacks](https://feeds.daemonfill.dev/crypto-hacks.xml) | Hacks and exploits with the amount lost and how it happened (DefiLlama) |
| [crypto-releases](https://feeds.daemonfill.dev/crypto-releases.xml) | Stable releases of Bitcoin Core, lnd, Geth, Lighthouse and Solana's Agave |
| [crypto-news](https://feeds.daemonfill.dev/crypto-news.xml) | CoinDesk, Cointelegraph and Decrypt, merged |

### Countries

Each feed labels items by outlet; state media is marked as such.

| Feed | What it follows |
| --- | --- |
| [thailand-news](https://feeds.daemonfill.dev/thailand-news.xml) | Thailand news in English (Khaosod English, Thai Enquirer) |
| [thailand-news-th](https://feeds.daemonfill.dev/thailand-news-th.xml) | ข่าวไทย: Thai-language news from Matichon and Prachachat |
| [thailand-disasters](https://feeds.daemonfill.dev/thailand-disasters.xml) | GDACS alerts for Thailand, Myanmar, Laos, Cambodia and Malaysia, any level |
| [thailand-earthquakes](https://feeds.daemonfill.dev/thailand-earthquakes.xml) | Earthquakes in and around Thailand (Thai Meteorological Department) |
| [japan-news](https://feeds.daemonfill.dev/japan-news.xml) | The Japan Times, The Mainichi and Japan Today |
| [china-news](https://feeds.daemonfill.dev/china-news.xml) | South China Morning Post and CGTN (Chinese state media) |
| [russia-news](https://feeds.daemonfill.dev/russia-news.xml) | TASS (Russian state media), Meduza and The Moscow Times |
| [india-news](https://feeds.daemonfill.dev/india-news.xml) | The Hindu and NDTV |
| [europe-news](https://feeds.daemonfill.dev/europe-news.xml) | POLITICO Europe and Euronews |
| [us-news](https://feeds.daemonfill.dev/us-news.xml) | NPR politics and PBS NewsHour |

### News

| Feed | What it follows |
| --- | --- |
| [world-headlines](https://feeds.daemonfill.dev/world-headlines.xml) | BBC, NPR and Al Jazeera headlines, merged |
| [climate-news](https://feeds.daemonfill.dev/climate-news.xml) | Climate and energy stories |

### Disasters and health

| Feed | What it follows |
| --- | --- |
| [earthquakes](https://feeds.daemonfill.dev/earthquakes.xml) | Significant earthquakes worldwide (USGS) |
| [disaster-alerts](https://feeds.daemonfill.dev/disaster-alerts.xml) | Orange and red GDACS alerts: earthquakes, cyclones, floods, volcanoes, droughts, wildfires |
| [hurricanes](https://feeds.daemonfill.dev/hurricanes.xml) | Atlantic and eastern Pacific hurricanes, each new National Hurricane Center advisory |
| [typhoons](https://feeds.daemonfill.dev/typhoons.xml) | Western Pacific and Indian Ocean typhoon warnings (Joint Typhoon Warning Center) |
| [tsunami-alerts](https://feeds.daemonfill.dev/tsunami-alerts.xml) | Tsunami bulletins and warnings from the US Tsunami Warning Centers |
| [volcanoes](https://feeds.daemonfill.dev/volcanoes.xml) | Weekly volcanic activity reports (Smithsonian Global Volcanism Program) |
| [disease-outbreaks](https://feeds.daemonfill.dev/disease-outbreaks.xml) | WHO Disease Outbreak News: Ebola, cholera, avian flu, mpox and more |
| [food-drug-recalls](https://feeds.daemonfill.dev/food-drug-recalls.xml) | US food, drug and medical device recalls (FDA) |

### Space

| Feed | What it follows |
| --- | --- |
| [space-launches](https://feeds.daemonfill.dev/space-launches.xml) | Rocket launches worldwide as soon as they are scheduled (Launch Library 2) |
| [nasa-image](https://feeds.daemonfill.dev/nasa-image.xml) | NASA Image of the Day |

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
