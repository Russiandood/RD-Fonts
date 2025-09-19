# GitHub Pages Webfont Scaffold

This folder is ready to publish your webfonts via GitHub Pages.

## File layout
```
/
  index.html            # smoke-test page
  /css
    fonts.css           # @font-face rules
  /webfonts             # your .woff2/.woff files
```

## Publish steps
1. Create a new GitHub repo (public) — or use an existing one.
2. Upload the contents of this folder to the root of that repo.
3. In the repo, go to **Settings → Pages** and set **Source** to "Deploy from a branch", Branch to `main`, Folder `/ (root)`.
4. Your site will appear at: `https://<user>.github.io/<repo>/`

## Use on your site
Reference the CSS from your page(s):
```html
<link rel="stylesheet" href="https://<user>.github.io/<repo>/css/fonts.css">
```
Then set the family in CSS:
```css
body { font-family: 'TT Octosquares Trl', system-ui, sans-serif; }
```

### Optional: jsDelivr CDN (version pinned)
- Tag a release in your repo (e.g. `v1.0.0`) and reference:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/<user>/<repo>@v1.0.0/css/fonts.css">
```
- Preload a font file:
```html
<link rel="preload" href="https://cdn.jsdelivr.net/gh/<user>/<repo>@v1.0.0/webfonts/TTOctosquaresTrl-Rg.woff2"
      as="font" type="font/woff2" crossorigin>
```

## Licensing
Ensure your font license allows public web hosting and redistribution. If it does not, keep the repo private and avoid GitHub Pages/CDNs.