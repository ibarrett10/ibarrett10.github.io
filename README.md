# ishaanbarrett.com

Academic portfolio site built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

## Quick Start — Deploy to GitHub Pages

### 1. Create the GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name the repo: `ishaanbarrett.com` (or `your-username.github.io` for the default GitHub Pages domain)
3. Set it to **Public**
4. Do **not** initialize with a README (we already have one)

### 2. Push This Site to GitHub

Unzip the downloaded folder, then from inside it:

```bash
cd ishaanbarrett.com
git init
git add .
git commit -m "Initial commit — academic portfolio"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ishaanbarrett.com.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. GitHub will auto-detect Jekyll and build the site

### 4. Connect Your Custom Domain

1. In your repo → **Settings** → **Pages** → **Custom domain**, enter: `ishaanbarrett.com`
2. At your domain registrar (e.g. Namecheap, Google Domains), add DNS records:

   | Type  | Name | Value                    |
   |-------|------|--------------------------|
   | A     | @    | 185.199.108.153          |
   | A     | @    | 185.199.109.153          |
   | A     | @    | 185.199.110.153          |
   | A     | @    | 185.199.111.153          |
   | CNAME | www  | YOUR_USERNAME.github.io  |

3. Check **Enforce HTTPS** once DNS propagates (can take up to 24 hours)

### 5. Add a CNAME File (optional — GitHub usually creates this)

If not auto-created, add a `CNAME` file in the repo root:

```
ishaanbarrett.com
```

## Local Development

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve

# Visit http://localhost:4000
```

## File Structure

```
├── _config.yml          # Site configuration
├── _data/
│   ├── publications.yml # Publications data (edit to add new pubs)
│   └── talks.yml        # Talks & editorials data
├── _includes/
│   ├── header.html      # Site header with navigation
│   └── footer.html      # Site footer
├── _layouts/
│   └── default.html     # Base HTML layout
├── assets/
│   ├── css/style.css    # All styles
│   └── js/main.js       # Mobile menu toggle
├── index.html           # About / Home page
├── cv.html              # Curriculum Vitae
├── publications.html    # Publications (reads from _data)
├── talks.html           # Talks & Writing (reads from _data)
├── contact.html         # Contact information
├── Gemfile              # Ruby dependencies
└── README.md            # This file
```

## Editing Content

- **Add a publication**: Edit `_data/publications.yml` — add a new entry at the top
- **Add a talk or editorial**: Edit `_data/talks.yml`
- **Update your bio**: Edit `index.html`
- **Update your CV**: Edit `cv.html`
- **Change styles**: Edit `assets/css/style.css`

## CV PDF

Replace the `#` href in `cv.html` with the path to your PDF:

```html
<a href="/assets/Barrett_CV.pdf" class="cv-download">
```

Place the PDF in `assets/`.
