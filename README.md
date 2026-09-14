# One-file game demos

A dependency-free collection of game design prototypes. Every demo is a standalone HTML file containing its own markup, CSS, and JavaScript.

## Add a demo

1. Duplicate `template.html` and give it a descriptive filename such as `prototype-grappling-hook.html`.
2. Build the interaction inside that one file.
3. Add a card linking to it in `index.html`.
4. Commit and push. GitHub Pages will publish the update automatically.

Use relative links (`prototype-name.html`) so the site works both locally and under a GitHub Pages project URL.

## Preview locally

Opening `index.html` directly is enough for simple demos. To match web hosting more closely, run a local server from this directory:

```powershell
python -m http.server 8000
```

Then open <http://localhost:8000>.

## Publish on GitHub Pages

1. Create an empty GitHub repository.
2. Push this folder to its `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Add one-file game demos"
   git branch -M main
   git remote add origin https://github.com/YOUR-NAME/YOUR-REPO.git
   git push -u origin main
   ```

3. On GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main**, folder **/(root)**, and save.

The site will appear at `https://YOUR-NAME.github.io/YOUR-REPO/`. GitHub may take a minute or two to perform the first deployment.

## Structure

```text
.
├── index.html                 # Public list of demos
├── demo-orbit-dodge.html      # Example standalone demo
├── template.html              # Copy this for a new demo
├── .nojekyll                  # Serve files as plain static content
└── README.md
```

There is no package manager, framework, or build command. That is the entire setup.
