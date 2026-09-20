# Vonamali Projects — website

Static site. No build step, no dependencies. Open `index.html` in a browser to preview it.

```
index.html   all page content
style.css    theme
assets/      logo, posters, album art, social share card
```

## Put it online (Netlify, free)

1. Go to https://app.netlify.com/drop
2. Drag this whole `site` folder onto the page.
3. It goes live in ~20 seconds at a `something-random.netlify.app` address.
4. Create a free Netlify account when prompted, so the site stays permanently.

## Point the domain at it

Chosen domain: **vonamaliprojects.in** — confirmed available at the .in registry
(whois.nixiregistry.in, checked 2026-09-20: "is available for registration").
Also free if you want to hold them: vonamali.in, vonamaliprojects.com, vonamali.com.

Note: Cloudflare Registrar does not sell `.in`. Use **Namecheap**, **GoDaddy**,
**BigRock** or **Hostinger** — roughly Rs. 500-900 for the first year. Turn on WHOIS
privacy so your address is not published. No Indian-address requirement for `.in`.

1. Buy `vonamaliprojects.in` at one of the registrars above.
2. In Netlify: **Site settings -> Domain management -> Add a domain** -> enter
   `vonamaliprojects.in`. Netlify shows a set of nameservers.
3. In the registrar's control panel, replace the existing nameservers with Netlify's.
4. Wait - usually under an hour, up to 24 hours. HTTPS is issued automatically.

## Editing

**Social links** — three places each in `index.html`; search for `youtube.com` and `instagram.com`.

**Add a film** — copy an `<article class="film">` block in `index.html` and change the
text, poster filename and badge.

**Add a song** — copy an `<li>` block inside `<ul class="albums">`. Point its `href` at the
specific YouTube video instead of the channel once each track has its own link.

**Replace an image** — drop the new file in `assets/`, update the `src` and the
`width`/`height` attributes (the real pixel size — they stop the page jumping while loading).

After any edit, drag the folder onto Netlify again, or connect the folder to a Git repo
for automatic updates.
