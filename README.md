# nobleworld.biz — Nebula Journal Archive

Static HTML/CSS site for **NEBULA: A Journal of Multidisciplinary Scholarship** (ISSN 1449-7751), published 2004–2011.

## Structure

```
nobleworld/
├── index.html            # Homepage (Nebula main)
├── whoweare.html         # Editorial & Advisory Boards
├── issues.html           # Browse issues by year/volume
├── africannebula.html    # African Nebula section (ISSN 1837-7963)
├── nebulab.html          # nebu[lab] section (ISSN 1838-1472)
├── css/
│   └── style.css         # Shared stylesheet
├── images/               # Banner and article images (add your own)
│   ├── banner-main.jpg       # Autumn forest — Nebula homepage & Who We Are
│   ├── banner-african.jpg    # Autumn trees — African Nebula
│   ├── banner-nebulab.jpg    # Dark nebula/space — nebu[lab]
│   ├── lab-cryptids.jpg      # Article image: Here Come the Cryptids!
│   └── lab-ontologies.jpg    # Article image: Superstar Ontologies
└── README.md
```

## Images: What to Add

Replace placeholder `<img src="...">` references with your actual downloaded images:

| File | Source |
|------|--------|
| `images/banner-main.jpg` | Autumn forest canopy from original site |
| `images/banner-african.jpg` | Autumn/orange tree from African Nebula |
| `images/banner-nebulab.jpg` | Dark nebula/space image from nebu[lab] |
| `images/lab-cryptids.jpg` | Eye image from nebu[lab] Feb 2011 |
| `images/lab-ontologies.jpg` | Red curtain image from nebu[lab] Feb 2011 |

Rename your downloaded images to match the filenames above and place them in the `images/` folder.

## Deploying to GitHub Pages

### 1. Create a new repository
- Go to github.com → New repository
- Name it `nobleworld.biz` (or any name you prefer)
- Set to Public
- Do NOT initialize with README (you have one)

### 2. Push the site
```bash
cd nobleworld
git init
git add .
git commit -m "Initial commit — Nebula journal archive"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/nobleworld.biz.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to repository → Settings → Pages
- Source: Deploy from a branch
- Branch: `main` → `/ (root)`
- Save

Your site will be live at: `https://YOUR-USERNAME.github.io/nobleworld.biz/`

### 4. Custom domain (nobleworld.biz)
- In Pages settings, enter `nobleworld.biz` in the Custom Domain field
- Add a `CNAME` file to the repo root containing just: `nobleworld.biz`
- At your domain registrar, add these DNS records:

```
A     @     185.199.108.153
A     @     185.199.109.153
A     @     185.199.110.153
A     @     185.199.111.153
CNAME www   YOUR-USERNAME.github.io
```

DNS propagation can take up to 48 hours. GitHub Pages will auto-provision HTTPS once the domain is verified.

## Populating Issues

The `issues.html` page uses placeholder volume/issue cards. To add article listings, you can either:

1. **Simple:** Add article titles directly into each `<div class="issue-card">` as plain text links
2. **Expanded:** Create individual issue pages (e.g. `issues/vol8no1.html`) and link the cards to them

## Notes
- All fonts load from Google Fonts (Playfair Display, EB Garamond, Raleway)
- No JavaScript dependencies — the site works without JS
- Fully responsive down to mobile
- nebu[lab] uses a distinct dark purple/cosmic theme matching the original
