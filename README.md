# Sunayana Samavedam — Academic Homepage

A minimal, typography-driven academic personal website.

## Structure

```
site/
├── index.html    ← The complete website (single file, static)
├── data.json     ← Structured resume data (reference for updates)
└── README.md     ← This file
```

## Run Locally

No build step required. Open `index.html` directly in a browser, or serve it:

```bash
# Python
cd site && python3 -m http.server 8000

# Node
npx serve site
```

Then visit `http://localhost:8000`.

## Update Content

All content is directly in `index.html`. To update:

1. Open `index.html` in any text editor
2. Edit the HTML content in the relevant section
3. Save and refresh

The `data.json` file is a structured reference of all resume data — use it as a guide when updating `index.html`, or as a base if you later want to migrate to a JS framework.

## Deploy

### GitHub Pages
1. Create a repo (e.g., `sunayana-981.github.io`)
2. Push the `site/` contents to the repo root
3. Enable Pages in Settings → Pages → Source: main branch
4. Site will be live at `https://sunayana-981.github.io`

### Vercel
1. Push to a GitHub repo
2. Import in [vercel.com](https://vercel.com)
3. Set output directory to `./` (root)
4. Deploy — Vercel will serve `index.html` automatically

### Netlify
1. Drag and drop the `site/` folder at [app.netlify.com/drop](https://app.netlify.com/drop)
2. Done.

## Customization

**Accent color**: Change `--c-accent` in the `:root` CSS block  
**Fonts**: Swap the Google Fonts `<link>` and update `--font-serif` / `--font-sans`  
**Max width**: Adjust `--max-w` (default: 780px)  
**Add a publication**: Copy an existing `.research-entry` block and edit the content  

## Design Decisions

- **Newsreader** (serif) for headings — academic, elegant, high readability
- **Source Sans 3** for body — clean, technical, pairs well with serif headings
- Monochrome palette with muted slate-blue accent (`#3d5a80`)
- Max-width 780px for optimal line length
- Left-aligned layout, no centered hero
- No JavaScript frameworks — pure static HTML/CSS
- Mobile-responsive with collapsible navigation
