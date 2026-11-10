# sleepyowlapps.github.io

The Sleepy Owl Apps website, served by GitHub Pages at
**https://sleepyowlapps.github.io**. Plain HTML and one stylesheet: no build
step. Upload or commit the files and the site updates within a minute or two.

## Layout

```
index.html              studio home: hero, apps grid, promises, contact
style.css               shared styles for every page
404.html                "page not found"
app-ads.txt             AdMob seller line (must stay at the site root)
assets/owl.svg          studio logo / favicon
volumebox/
  index.html            Volume Box page
  privacy-policy.html   Volume Box privacy policy (the URL given to Google Play)
  icon.svg              app icon
  screens/*.jpg         screenshots (540 px wide)
privacy-policy.html     old address, redirects to volumebox/privacy-policy.html
```

## Add a new app

1. **Copy the folder:** duplicate `volumebox/` and rename it to the app's short name
   (lowercase, no spaces), e.g. `sleeptimer/`.
2. **Edit the app page** (`<new>/index.html`):
   - title, description and texts;
   - the accent colours on `<body style="--accent:#...; --accent-2:#...">`;
   - features, FAQ and the "How it stays free" section;
   - the Play button: replace the disabled "Coming soon" button with
     `https://play.google.com/store/apps/details?id=<application id>` once live.
3. **Write its privacy policy** (`<new>/privacy-policy.html`). Each app needs its own,
   describing exactly what that app does. Give this URL to Google Play.
4. **Replace the icon and screenshots** (`icon.svg`, `screens/`). Keep screenshots around
   540 px wide so pages stay fast.
5. **Add a card on the home page:** in `index.html`, copy the Volume Box `<article
   class="card app-card">` block inside the apps grid, then change the links, icon, texts
   and `--card-accent`. Keep the "More apps coming" card last (or remove it).
6. **Footer links:** add the new app to the footer in `index.html`.

## app-ads.txt

One line per ad account. All apps from the same AdMob account share it:

```
google.com, pub-9539817856475993, DIRECT, f08c47fec0942fa0
```

Add another line only if a different ad network or account is used. Every app's Play
listing must use `https://sleepyowlapps.github.io` as its website so AdMob finds this file.

## Contact

sleepyowlapps8@proton.me
