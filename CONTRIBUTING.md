# Adding a feed

Every feed here is one pipeline file in [`feeds/`](feeds). To add one:

1. Install UnlimitedPipe (`curl -fsSL https://raw.githubusercontent.com/Fuyuki0/unlimitedpipe/main/install.sh | sh`),
   then find the best way to read the source:
   `unlimited inspect https://example.gov/news` shows its feeds, JSON APIs, product data and
   what robots.txt allows.
2. Copy a similar file from `feeds/` (an RSS merge, a JSON API, a GitHub releases list) or let
   `unlimited new URL` write a first version. Outputs go to `../public/NAME.xml` and `.json`.
3. Check it:
   ```bash
   unlimited run feeds/NAME.yml --validate
   UNLIMITEDPIPE_STATE_DIR=/tmp/state unlimited run feeds/NAME.yml   # first run: items
   UNLIMITEDPIPE_STATE_DIR=/tmp/state unlimited run feeds/NAME.yml   # second run: nothing new
   ```
4. Add a row to the README table and open a pull request. The template has a short checklist.

## What a good feed is

- **Public and allowed.** Official feeds and APIs first. A web page only when its robots.txt
  allows it. Nothing behind a login or paywall, and no working around blocks.
- **About institutions, not private people.** Companies, governments, public officials acting
  in office, software projects, natural events.
- **Readable titles.** Each item should make sense in a feed reader on its own: the company or
  country first, then what happened, with amounts where they matter.
- **Quiet.** Filter out routine noise (scheduled maintenance, weekly statistics) so every item
  is worth a look.
- **Labeled.** When a feed merges sources, say which outlet each item comes from, and mark
  state media as such.

Not sure? [Request a feed](../../issues/new?template=feed-request.yml) instead and describe
what you would like to follow.
