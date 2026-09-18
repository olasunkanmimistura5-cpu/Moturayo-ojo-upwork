# Motunrayo Olasunkanmi — Book Editor Website

A single-page portfolio site for a Christian nonfiction book editor. Static HTML,
no build step, no dependencies. Designed to be hosted free on GitHub Pages.

---

## 1. Files in this repo

| File | What it does |
|---|---|
| `index.html` | The entire website — HTML, CSS, JavaScript and structured data in one file. |
| `assets/motunrayo.jpg` | Portrait used in the About section and in social link previews. |
| `robots.txt` | Tells search engines **and AI answer engines** they may crawl the site. |
| `sitemap.xml` | Lists the page and its sections for search engines. |
| `llms.txt` | A plain-text brief written for AI assistants (ChatGPT, Claude, Perplexity). |
| `README.md` | This file. |

---

## 2. Put it online in 10 minutes

1. Sign in at [github.com](https://github.com) and click **New repository**.
2. Name it exactly `YOUR-USERNAME.github.io` — replacing `YOUR-USERNAME` with your
   real GitHub username. Set it to **Public**. Do not tick "Add a README".
3. Click **uploading an existing file** on the next screen.
4. Drag in `index.html`, `robots.txt`, `sitemap.xml`, `llms.txt`, `README.md`,
   **and the `assets` folder** (drag the whole folder so the image keeps its path).
5. Click **Commit changes**.
6. Go to **Settings → Pages**. Under *Source*, choose **Deploy from a branch**,
   branch `main`, folder `/ (root)`. Save.
7. Wait 1–3 minutes. Your site is live at `https://YOUR-USERNAME.github.io/`.

> If you name the repo something else (e.g. `book-editor`), the address becomes
> `https://YOUR-USERNAME.github.io/book-editor/` and you must use that full
> address everywhere in step 3 below.

---

## 3. Required: replace the placeholder address

The files contain the placeholder `YOUR-USERNAME.github.io`. Search engines and
AI assistants need the real address to index and cite the site correctly.

On GitHub: open each file, click the pencil icon, use **Ctrl+F / Cmd+F** to find
`YOUR-USERNAME`, replace every occurrence with your username, then commit.

Files to update: `index.html`, `robots.txt`, `sitemap.xml`, `llms.txt`.

---

## 4. Using your own domain (optional)

1. Buy a domain (e.g. `motunrayoedits.com`).
2. In your domain registrar's DNS settings, add four `A` records pointing to:
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
3. In GitHub **Settings → Pages → Custom domain**, enter the domain and save.
   Tick **Enforce HTTPS** once it becomes available.
4. Replace the GitHub address with your domain everywhere (see step 3 above).

---

## 5. Things you will want to change

| What | Where |
|---|---|
| Your displayed name | `index.html` — search for `Motunrayo Olasunkanmi` and replace throughout, including in the JSON-LD block near the bottom. |
| Your photo | Replace `assets/motunrayo.jpg` with a new file of the same name. |
| Prices and turnaround | FAQ section — search for `$10 per hour` and `50,000-word`. |
| The sample before/after | Search the `<script>` for `var before =` and `var after =`. |
| WhatsApp number | Search for `2349157352302` (used in links) and `+234 915 735 2302` (displayed). |
| Email | Search for `olasunkanmimistura5@gmail.com`. |
| Upwork link | Search for `upwork.com/freelancers`. |

### Adding client testimonials later

Real reviews are the single biggest thing this site is currently missing. Once you
have permission to quote a client, add a section and also add this to the
`"@graph"` array in the JSON-LD block so Google can show star ratings:

```json
{
  "@type":"Review",
  "itemReviewed":{"@id":"https://YOUR-USERNAME.github.io/#business"},
  "author":{"@type":"Person","name":"Client name"},
  "reviewRating":{"@type":"Rating","ratingValue":"5","bestRating":"5"},
  "reviewBody":"What the client actually said."
}
```

Only add reviews you genuinely received — fake review markup gets sites penalised.

---

## 6. How SEO, AEO and GEO are handled here

**SEO — traditional search (Google, Bing).**
Descriptive title and meta description built around the real search phrase
("Christian nonfiction book editor"), one `<h1>`, a clean heading hierarchy,
canonical URL, Open Graph and Twitter cards, descriptive image alt text,
`sitemap.xml`, `robots.txt`, fast single-file load with no frameworks, and a
fully responsive, keyboard-accessible layout — mobile usability and speed are
ranking factors.

**AEO — answer engine optimisation (featured snippets, voice answers).**
Content is written as direct questions with direct answers. The "What a book
editor actually does" block leads with a short, quotable answer. `FAQPage`
structured data marks up 15 questions so Google can lift them straight into
results, and `HowTo` markup describes the five-step process.

**GEO — generative engine optimisation (ChatGPT, Claude, Perplexity, AI Overviews).**
AI crawlers are explicitly allowed in `robots.txt` — most sites silently block
them and lose the recommendations. `llms.txt` gives assistants a clean factual
brief they can quote. A `ProfessionalService` + `Person` schema graph states
services, location, languages, price range and areas served as machine-readable
facts, so an assistant asked "who can edit my devotional?" has something specific
to cite. Concrete numbers (1,000-word sample, $10/hour, 1–4 week turnarounds) are
stated in plain text, because generative engines quote specifics and skip vague
claims.

**After you publish, do these three things:**
1. Add the site to [Google Search Console](https://search.google.com/search-console)
   and submit `sitemap.xml`.
2. Add it to [Bing Webmaster Tools](https://www.bing.com/webmasters) — Bing feeds
   ChatGPT search results.
3. Put the link in your Upwork profile, WhatsApp bio, email signature and every
   social profile. Links from places you already control are the fastest way to
   get indexed.

---

## 7. Technical notes

- No cookies, no analytics, no trackers, no backend. The contact form builds a
  WhatsApp or email message in the visitor's own app; nothing is stored or sent
  to a server, which is why the site needs no privacy policy or consent banner.
- Fonts load from Google Fonts. Everything else is self-contained.
- Respects `prefers-reduced-motion`, has visible keyboard focus rings, and meets
  colour-contrast requirements.
- Tested down to 320px width.

---

© Motunrayo Olasunkanmi. Site content is yours to edit freely.
