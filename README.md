# Academic Website — Setup Guide

This is a Quarto-based academic website ready to deploy on GitHub Pages for free.

---

## 🚀 Step-by-step setup (30 minutes)

### 1. Create a GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it **`yourusername.github.io`** (replace with your actual GitHub username)
3. Set it to **Public**
4. Click **Create repository**

### 2. Upload these files

Option A — via the GitHub web interface (no terminal needed):
1. Open your new repository
2. Click **Add file → Upload files**
3. Drag and drop all the files and folders from this zip
4. Click **Commit changes**

Option B — via terminal (if you know Git):
```bash
git init
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git add .
git commit -m "Initial website"
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repository → **Settings → Pages**
2. Under **Source**, select **GitHub Actions**
3. Save

### 4. Wait ~2 minutes

GitHub will automatically build and publish your site.
Your website will be live at: **https://yourusername.github.io**

---

## ✏️ How to update content

All content is in plain text files (`.qmd`). You can edit them directly on GitHub:

| File | What it controls |
|------|-----------------|
| `index.qmd` | Homepage: your name, bio, research interests |
| `publications/index.qmd` | Your articles and book chapters |
| `talks/index.qmd` | Conference presentations and invited talks |
| `awards/index.qmd` | Awards, grants, distinctions |
| `_quarto.yml` | Site title, navigation, your links |

To edit: open the file on GitHub → click the ✏️ pencil icon → edit → **Commit changes**.
The website rebuilds automatically within ~2 minutes.

---

## 🖼️ Adding your profile photo

1. Rename your photo to `profile.jpg`
2. Upload it to the `assets/` folder
3. It will appear automatically on the homepage

---

## 📄 Adding PDFs (papers, slides)

Upload PDF files to:
- `assets/papers/` — for journal articles
- `assets/slides/` — for presentation slides
- `assets/posters/` — for conference posters

Then reference them in the `.qmd` files as:
```
[PDF](assets/papers/your-file.pdf)
```

---

## 🔗 Updating your links

Open `_quarto.yml` and replace:
- `yourusername` → your GitHub username
- `your@email.com` → your institutional email

Open `index.qmd` and replace:
- `Your Name` → your name
- `Your Institution` → your institution
- The research interests bullet points with your actual topics
- The Google Scholar URL with your own

---

## 🎨 Changing the colour theme

In `_quarto.yml`, the `theme` field accepts any Bootswatch theme.
Options that work well for academic sites: `flatly`, `cosmo`, `litera`, `journal`, `united`.

Change `flatly` to any of the above and push — the site rebuilds automatically.

Full list: https://bootswatch.com/

---

## 💡 Tips for atmospheric sciences

- Link your **ORCID** in the navbar: add `href: https://orcid.org/0000-0000-0000-0000` with icon `orcid`
- Link **ResearchGate** or **ResearcherID** if you use them
- For each publication, include the DOI — it makes Google Scholar index your page
- The BibTeX block in publications lets visitors cite your work with one click
