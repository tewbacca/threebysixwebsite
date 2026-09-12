# 3by6.app

Marketing site for 3 by 6, hosted on GitHub Pages at [3by6.app](https://3by6.app).

## Structure

- `index.html` — landing page
- `privacy.html`, `support.html` — required App Store submission pages
- `styles.css`, `script.js` — shared styling/behaviour
- `assets/` — app icon exports
- `CNAME` — custom domain for GitHub Pages

## Local preview

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploying

1. Push this repo to GitHub as a **public** repository.
2. In the repo's **Settings → Pages**, set the source to the `main` branch, `/ (root)` folder.
3. At your domain registrar, point `3by6.app` at GitHub Pages:
   - Four `A` records at the apex (`@`) to:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Optionally a `CNAME` record for `www` pointing to `<your-github-username>.github.io`
4. Back in **Settings → Pages**, confirm the custom domain shows `3by6.app` and enable **Enforce HTTPS** once the certificate is issued.

## Before submitting to the App Store

- Update the App Store badge link in `index.html` from `#` to the real App Store listing URL once the app is live.
- Support and privacy contact both route to the Pilea Studio Jira form (`support.html`) — it can't be embedded as an iframe (Atlassian sends `X-Frame-Options: SAMEORIGIN`), so it opens as a link instead.
- Swap the placeholder board items in the "board demo" on the home page for a real screenshot once one exists.
