# Abhilash Antony — Portfolio Website

A responsive, single-page portfolio for Abhilash Antony, Associate Software Engineer (AI & Data Science). Built with plain HTML, CSS and JavaScript so it can be previewed without installing a frontend framework and deployed directly to GitHub Pages.

## What's included

- Responsive portfolio sections: intro, outcomes, about, selected work, experience, skills, education and contact.
- Project category filters and mobile navigation.
- Accessible navigation labels, reduced-motion support, SEO metadata and a custom favicon.
- Resume download (`documents/Abhilash_Antony_Resume.docx`).
- No npm packages or build step required.

## 1. Preview locally

### Option A — Python (recommended)

1. Extract the ZIP file.
2. Open a terminal in the extracted `abhilash-portfolio` folder.
3. Run one of the following commands:

   **Windows:**
   ```bash
   py -m http.server 5500
   ```

   **macOS / Linux:**
   ```bash
   python3 -m http.server 5500
   ```

4. Open <http://localhost:5500> in your browser.
5. Stop the local server with `Ctrl+C` in the terminal.

If `py` or `python3` isn't available, you can open the folder in Visual Studio Code and use the **Live Server** extension. Because this is a static site, there is no `npm install` or compilation step.

## 2. Put it on GitHub

1. Sign in to GitHub and create a new repository. For the simplest setup, name it `abhilash-antony.github.io` if that repository name is available to you. Otherwise, use a name such as `abhilash-portfolio`.
2. For the cleanest first push, create the repository without adding a README, licence or `.gitignore` on GitHub.
3. In a terminal, change directory to the extracted `abhilash-portfolio` folder and run:

   ```bash
   git init
   git add .
   git commit -m "Add portfolio website"
   git branch -M main
   git remote add origin https://github.com/abhilash-antony/abhilash-antony.github.io.git
   git push -u origin main
   ```

   If you chose a different repository name, replace `abhilash-antony.github.io` in the remote URL with that name. If your GitHub username/repository differs, use the matching URL shown on the repository's **Code** button.

## 3. Deploy with GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Select branch **`main`** and folder **`/ (root)`**, then click **Save**.
5. Wait for the Pages deployment to finish. Its status is visible in the repository's **Actions** tab and in **Settings → Pages**.

The site URL will normally be:

- If the repository is named `abhilash-antony.github.io`: <https://abhilash-antony.github.io/>
- If it has another name (for example, `abhilash-portfolio`): `https://abhilash-antony.github.io/abhilash-portfolio/`

After the first deploy, future commits pushed to `main` will update the published site automatically. A new deployment may take a short time to appear.

## Personalise before publishing

- **Headshot:** the file named `Abhilash PP.jpg` was not present among the files available for this build. For the initial preview, the website uses the portrait already shown on your existing portfolio URL. To make the website self-contained, copy your desired photo into `assets/Abhilash PP.jpg`, then change the `src` of the `<img data-portrait>` element near the top of `index.html` to `assets/Abhilash%20PP.jpg`. You can delete the external image preconnect line once switched to the local image. If the remote portrait fails to load, a local initials illustration is used as a fallback.
- **Resume:** replace `documents/Abhilash_Antony_Resume.docx` when you update your resume. Keep the filename the same, or update the download link in `index.html`.
- **Links:** confirm your LinkedIn, GitHub and project links before publishing.
- **Project descriptions and metrics:** descriptions are based on your provided resume and LinkedIn/portfolio profile; update any details that change.

## File structure

```text
abhilash-portfolio/
├── index.html
├── styles.css
├── script.js
├── README.md
├── .nojekyll
├── assets/
│   ├── avatar.svg
│   └── favicon.svg
└── documents/
    └── Abhilash_Antony_Resume.docx
```

## Notes

- This is a static client-side site. It has no backend, database, API secrets or environment variables.
- The layout works as a GitHub Pages project site as long as links to local assets remain relative.
- Google Fonts are loaded from a CDN; the site falls back to system fonts if that service is unavailable.
