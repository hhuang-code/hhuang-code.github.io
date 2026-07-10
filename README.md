# Academic Homepage

Static personal website (plain HTML + CSS, no build step). Design inspired by a Google Sites
academic page but written from scratch — easy to edit locally and host free on GitHub Pages.

## Structure
```
index.html          Academic (home)
publications.html   Publications
teaching.html       Teaching
realme.html         Personal
assets/style.css    All styling (edit colors at the top under :root)
assets/img/         Images — replace the .svg placeholders with your own .jpg/.png
.nojekyll           Tells GitHub Pages to serve files as-is
```

## Edit locally
Just open `index.html` in a browser. For live reload, run a local server:
```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
Edit the HTML text directly, and change theme colors in `assets/style.css` (the `:root` block).

### Replacing images
The pages reference `.jpg` files but placeholder `.svg` files are provided. Either:
- drop in real images named e.g. `assets/img/profile.jpg`, `g1.jpg`, `pub1.jpg`, or
- keep the SVGs and point the HTML `src` at the `.svg` names.

## Deploy to GitHub Pages
1. Create a repo named `<your-username>.github.io` (for a user site) or any repo (for a project site).
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo>.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source: Deploy from a branch → main / (root) → Save**.
4. Your site appears at `https://<your-username>.github.io/` (user site) or
   `https://<your-username>.github.io/<repo>/` (project site) within a minute or two.
