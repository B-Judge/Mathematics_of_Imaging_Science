# Mathematics of Imaging Science

Interactive study walkthroughs for BME 5700, based on Harrison H. Barrett & Kyle J. Myers,
*Foundations of Image Science* (Wiley, 2004).

The repository is a static website: `index.html` is the landing page, and each walkthrough is a
self-contained HTML page in `walkthroughs/`.

| Walkthrough | File |
| --- | --- |
| Imaging Science Field Guide | [`walkthroughs/imaging-science-field-guide.html`](walkthroughs/imaging-science-field-guide.html) |
| Fourier Coil Atlas | [`walkthroughs/fourier-coil-atlas.html`](walkthroughs/fourier-coil-atlas.html) |

## Publishing with GitHub Pages

1. On GitHub, open **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to *Deploy from a branch*.
3. Pick the branch (e.g. `main`) and the `/ (root)` folder, then **Save**.

The site appears at `https://<username>.github.io/<repository-name>/` within a minute or two.
No build step is needed (`.nojekyll` tells GitHub to serve the files as-is).

## Adding a new walkthrough

1. Save the page in `walkthroughs/`, using a lowercase-with-dashes name, e.g. `walkthroughs/sampling-theory.html`.
2. In `index.html`, copy one of the existing `<li>…</li>` cards inside `<ul id="walkthroughs">`,
   paste it above the "More on the way" card, and update the link, label, title, description and tags.
   The walkthrough count on the landing page updates on its own.
3. Optional: add a link back to the landing page at the top of the new page, matching the others:

   ```html
   <a class="eyebrow site-home" href="../index.html">&larr; All walkthroughs</a>
   ```

## Viewing locally

Open `index.html` in a browser, or run a small local server from the repository folder:

```bash
python3 -m http.server 8000
```

then visit <http://localhost:8000>.
