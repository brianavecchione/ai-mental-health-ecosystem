# AI × Mental Health — Ecosystem Map

**A living, open-source landscape of organizations, researchers, advocates, policymakers, and communities shaping how AI intersects with mental health, therapy, and emotional wellbeing.**

🔗 **[View the live map →](https://YOUR_USERNAME.github.io/YOUR_REPO)**

---

## What this is

This project maps the stakeholder ecosystem around AI and mental health — from consumer chatbot apps and clinical AI tools to civil society watchdogs, impacted communities, policy bodies, and funders. It's designed to be a shared resource: useful for researchers, advocates, journalists, policymakers, and anyone trying to understand who's operating in this space and how they relate.

Organizations are tagged with one or more categories, and the map is fully searchable and filterable.

**Categories covered:**
- Consumer Apps (B2C)
- Clinical & Enterprise (B2B)
- Research & Academia
- Nonprofits & Advocacy
- Policy & Government
- Investors & Funders
- Civil Society & NGOs
- Professional Associations
- Media, Journalists & Influencers
- Philanthropy
- Private Sector / Tech
- Impacted Communities

---

## How to suggest a new entry

**[→ Open an Issue using the "Suggest an Organization" template](../../issues/new?template=add-organization.yml)**

You'll be asked for: the org's name, URL, category, a short description, and relevant tags. A maintainer will review and add it to `orgs.json`.

We're especially looking for entries in underrepresented categories:
- **Impacted Communities** — user groups, peer support networks, survivor communities
- **Global / non-US orgs** — regulatory bodies, civil society groups, and research labs outside North America
- **Philanthropy & Funders** — foundations and grant-makers active in this space

---

## How to update an existing entry

If you spot an error, outdated information, or a missing category tag for an existing org, please [open an Issue](../../issues/new) with the title `[UPDATE] Org Name` and describe what needs to change.

---

## Data structure

All organization data lives in [`orgs.json`](orgs.json). Each entry follows this schema:

```json
{
  "name": "Organization Name",
  "cats": ["policy", "civil"],
  "type": "Short entity type label",
  "desc": "2–4 sentence description of the org and its relevance to AI and mental health.",
  "tags": ["tag1", "tag2", "tag3"],
  "url": "https://example.org"
}
```

**Valid `cats` values:**
`consumer` · `clinical` · `research` · `nonprofit` · `policy` · `investors` · `civil` · `professional` · `media` · `philanthropy` · `private` · `community`

An organization can belong to multiple categories.

---

## Running locally

This is a static site — just serve the directory with any local web server:

```bash
# Python
python3 -m http.server 8000

# Node (npx)
npx serve .

# VS Code
# Use the "Live Server" extension
```

Then open `http://localhost:8000` in your browser.

> **Note:** Opening `index.html` directly via `file://` won't work because `fetch()` is blocked by the browser for local files. You need a web server.

---

## Deploying to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set Source to **Deploy from a branch**, select `main`, folder `/` (root)
4. Your map will be live at `https://YOUR_USERNAME.github.io/YOUR_REPO`

Update the `contribute-btn` link in `index.html` and the link in this README to point to your actual repo URL.

---

## Contributing guidelines

- Keep descriptions factual, neutral, and specific — focus on what the org *does* in this space, not PR language from their website
- Include organizations critical of AI in mental health, not just boosters — the map should reflect the full ecosystem
- When in doubt about categories, an org can belong to more than one
- Impacted community groups and grassroots orgs are especially welcome — they're often underrepresented in landscapes like this

---

## License

Data (`orgs.json`) is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use, share, and adapt with attribution.

Code (`index.html`) is released under [MIT License](LICENSE).
