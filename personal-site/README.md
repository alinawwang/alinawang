# Personal site (Jekyll + GitHub Pages)

A multi-page site: Home (hero + About) plus separate pages for
Education, Research, Projects, Skills, Leadership, and Contact.
Content lives in `_data/*.yml` so you can add or edit entries
without touching HTML.

## Pages

- `/` — `index.html` (hero + About blurb)
- `/education/` — `education/index.html`
- `/research/` — `research/index.html`
- `/projects/` — `projects/index.html`
- `/skills/` — `skills/index.html`
- `/leadership/` — `leadership/index.html`
- `/contact/` — `contact/index.html`

Each page pulls its list content from the matching `_data/*.yml` file,
so adding a new research entry, project, or role means editing the
YAML, not the HTML.

## 1. Fill in your info

- `_config.yml` — name, tagline, email, GitHub username, LinkedIn URL, resume path
- `_data/research.yml` — research positions
- `_data/projects.yml` — projects (leave `link:` blank to skip a link)
- `_data/leadership.yml` — org roles
- `_data/skills.yml` — skill tags by category
- `index.html` — the About paragraph (search for the `[Write 3–4 sentences...]` placeholder)
- Drop a resume PDF at `assets/resume.pdf` if you want the Contact link to work

## 2. Publish with GitHub Pages

1. Create a new GitHub repo named `<your-username>.github.io`
   (must match your username exactly for the free user-site URL).
2. Push this folder's contents to that repo's `main` branch:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. In the repo settings → Pages, set the source to the `main` branch
   (root). GitHub Pages will detect Jekyll automatically — no build
   step needed on your end.
4. Your site will be live at `https://<your-username>.github.io`
   within a minute or two.

## 3. Preview locally (optional)

Requires Ruby + Bundler.

```
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Notes

- The design uses IBM Plex Mono (headings/labels) and IBM Plex Serif
  (body text), loaded from Google Fonts in `_layouts/default.html`.
- Colors and type live as CSS variables at the top of
  `assets/css/main.scss` if you want to adjust the palette.
- Dashed lines between sections are a deliberate nod to cut lines /
  blueprint drafting — feel free to change if it's not your taste.
