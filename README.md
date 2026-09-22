# Before It Grew Quiet — website

Portfolio-grade static website for the game.

## Open it
Double-click `index.html`.

## Files
- `index.html` — structure/content
- `styles.css` — visual design and responsive layout
- `script.js` — language switch, animations, lightbox, form validation
- `assets/` — favicon and future screenshots
- `assets/screenshots/` — put real gameplay screenshots here

## Replacing placeholder screenshots
The current gallery is intentionally made of CSS placeholder art so the site never pretends to show real gameplay.

When you have screenshots:
1. copy JPG/PNG files into `assets/screenshots/`
2. in `index.html`, replace a `.shot-placeholder` block with e.g.
   `<img src="assets/screenshots/farm-01.jpg" alt="Gameplay on the farm">`
3. add in CSS:
   `.shot img { width:100%; height:100%; object-fit:cover; display:block; }`

## Adding the trailer
Replace the `.video-placeholder` element in `index.html` with a YouTube embed:

```html
<div class="video-embed">
  <iframe
    src="https://www.youtube.com/embed/VIDEO_ID"
    title="Before It Grew Quiet gameplay trailer"
    allowfullscreen>
  </iframe>
</div>
```

and add:

```css
.video-embed{aspect-ratio:16/9}
.video-embed iframe{width:100%;height:100%;border:0;border-radius:25px}
```

## Connecting the contact form
The demo validates the form but intentionally does not send personal data.

Simple production options:
- Formspree
- Netlify Forms
- your own PHP/Node/backend endpoint

Do not publish a real email address in JavaScript if you want to reduce spam.

## Polish / English
Text strings live in the `translations` object inside `script.js`. Edit both `en` and `pl`.

## Portfolio note
This build is intentionally framework-free (HTML/CSS/JS), so it loads fast and can be hosted almost anywhere: GitHub Pages, Netlify, Cloudflare Pages, Vercel, shared hosting, etc.
