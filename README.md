# Yuan Wu's website

Source for my personal website. It is built with Jekyll from the
[academic-website-template](https://github.com/sbryngelson/academic-website-template)
by Spencer Bryngelson (MIT license; see `LICENSE`).

## How to update the site

Edit a file on GitHub (pencil icon, then "Commit changes") or push from your
computer to the `source` branch. A GitHub Actions workflow rebuilds and
publishes the site in a few minutes. Check the **Actions** tab if a change does
not show up.

## Where things live

| To change | Edit |
|---|---|
| Name, title, institution, email, photo, links, accent color | `_config.yml` |
| Home page text and research-area chips | `_pages/home.md` |
| Publications | `assets/ref.bib` (PDFs go in `papers/`) |
| News in the sidebar | `_data/news.yml` (newest first) |
| Education | `_data/pi.yml` |
| Awards on the Education page | `_data/awards.yml` |
| CV | put `cv.pdf` in `papers/`, then set `links: cv: "papers/cv.pdf"` in `_config.yml` |
| Profile photo | put the image in `images/`, then set `photo:` in `_config.yml` |

## Publication entries

Each entry in `assets/ref.bib` is shown as title, authors (full names) and
venue on separate lines. The venue is the entry's `booktitle`, `journal` or
`note`. Besides the usual BibTeX fields, these control how an entry looks
(they are left out of the BibTeX that visitors copy):

| Field | Effect |
|---|---|
| `equal = {Yuan Wu and Mairui Li}` | asterisk after each listed author (equal contribution) |
| `displayyear = {2026}` | year shown in the badge, if different from `year` |
| `acceptance = {13.5}` | adds "(Paper acceptance rate: 13.5%)" after the venue |
| `acceptancetrack = {Main conference}` | replaces the word "Paper" in that note |
| `selected = {true}` | also listed under "Selected publications" on the home page |
| `arxiv`, `doi`, `url` | arXiv, DOI and Link buttons |
| `code`, `slides`, `video`, `poster`, `data` | buttons with those names (give a URL) |
| `file = {paper.pdf}` | PDF button; put the file in `papers/` |
| `abstract` | expandable Abstract button |
| `annotation` | one small line of text under the venue |

## Pages

The navbar has Home, Publications and Education. The template's group-oriented
pages (Team, Talks, Teaching, Software, Research, Blog) were removed. To bring
one back, copy its file from the template's
[`_pages/`](https://github.com/sbryngelson/academic-website-template/tree/source/_pages)
folder and uncomment its line under `nav_pages` in `_config.yml`.

## Previewing on your own computer (optional)

Install Ruby 3.2 or newer, then:

```bash
bundle install
bundle exec jekyll serve   # open http://localhost:4000
```
