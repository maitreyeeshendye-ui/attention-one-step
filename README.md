# Self-attention, one step at a time

Interactive walkthrough of one encoder-style attention head, following “it” in:
“A cat sat on a mat because it was tired.”

## Deploy on GitHub Pages (no build required)

1. Create a GitHub repository, for example `attention-one-step`. A public repository works with GitHub Free.
2. Upload the CONTENTS of this folder to the repository root. `index.html`, `style.css`, and `app.js` must sit together at the top level, not inside another folder. Do not upload the ZIP itself.
3. Commit the files to `main`.
4. Open repository **Settings > Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select branch **main** and folder **/(root)**, then **Save**.
7. Wait for deployment to finish. Pages settings will show your website link, normally `https://YOUR-USERNAME.github.io/attention-one-step/`.

GitHub instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Run locally

Double-click `index.html` to open it in a browser. No Node, npm, API key, backend, or installation is needed.

Alternatively, run `python -m http.server 8000` in this folder and open http://localhost:8000.

## Files

- `index.html`: page structure and explanatory text
- `style.css`: layout, colors and responsive styling
- `app.js`: attention calculations and seven-step interaction
- `.nojekyll`: bypasses Jekyll processing on GitHub Pages

## Controls

Use Next / Back, click a step, or use the left/right arrow keys. Select available example tokens in the vector/projection/score views. Start again returns to the beginning.

## Teaching scope

This is a numerical teaching example, not a trained model. Each word stands in for one token. Input vectors and projection matrices are hand-chosen. It uses one encoder-style head, so “it” can attend to later words such as “tired”. A causal GPT head at that position could not do that. Attention weights mix value vectors; they are not probabilities of pronoun reference. The final output is a contextual vector, not a generated word.

## Editing

Change appearance in `style.css`. Calculations, vectors, matrices and step content live in `app.js`. After committing updates, GitHub Pages republishes them.
