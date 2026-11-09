# Workflow Discovery landing page

A single static landing page: `index.html` plus `styles.css`. It has no build step, no dependencies, and no JavaScript. The look follows [kendrahartnett.com](https://kendrahartnett.com), and the navigation links point back to that site.

## View it locally

The quickest way is to open `index.html` in a browser by double-clicking it.

To view it at a local URL instead, start a small server from this folder:

```sh
python -m http.server 8000
```

Then open http://localhost:8000.

## Deploy to GitHub Pages

1. Push this repo to GitHub:
   ```sh
   git add index.html styles.css README.md
   git commit -m "Landing page"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. On GitHub, open the repo and go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**. Then choose branch `main` and folder `/ (root)`, and click **Save**.
4. After a minute or two the page will be live at `https://<your-username>.github.io/<repo-name>/`.

Every push to `main` redeploys the page. If you want it on a custom subdomain (for example `start.kendrahartnett.com`), add that domain under **Settings → Pages → Custom domain**. Then create a matching CNAME record with your DNS provider.
