# Piranesi — Dedalus Website

## GitHub Pages Setup

1. Create a GitHub account at https://github.com if you don't have one
2. Create a new repository named exactly: `yourusername.github.io`
   (replace "yourusername" with your actual GitHub username)
3. Set the repository to **Public**
4. Upload all files in this folder to the repository root
   - You can drag and drop files directly in the GitHub web interface
   - Or use GitHub Desktop (free app) for easier file management
5. Your site will be live at `https://yourusername.github.io`

## File Structure

```
/
├── index.html          ← Home / Landing page
├── songs.html          ← All five songs with lyrics and stories
├── dedalus.html        ← Artist bio and discography
├── links.html          ← All external links
├── contact.html        ← Contact form
├── css/
│   └── style.css       ← All styles
├── js/
│   └── main.js         ← Navigation, scroll animations
└── images/             ← All artwork and branding images
```

## Adding Audio Players

When your songs are on Bandcamp, you can embed individual track players.
On Bandcamp, go to each track → Share/Embed → copy the iframe embed code.
Replace the `<div class="media-placeholder">` block in songs.html with the iframe.

Example Bandcamp embed:
```html
<iframe style="border: 0; width: 100%; height: 120px;"
  src="https://bandcamp.com/EmbeddedPlayer/track=TRACKID/size=large/bgcol=000000/linkcol=b8973a/tracklist=false/artwork=small/"
  seamless>
</iframe>
```

## Adding Videos

When you have YouTube videos, replace the `<div class="video-placeholder">` block with:
```html
<div class="video-embed">
  <iframe width="100%" height="400"
    src="https://www.youtube.com/embed/VIDEO_ID"
    frameborder="0" allowfullscreen>
  </iframe>
</div>
```

## Contact Form Setup (Formspree)

The contact form needs a free backend service to send emails.
1. Go to https://formspree.io and create a free account
2. Create a new form — you'll get a form endpoint URL
3. In contact.html, update the form tag:
   ```html
   <form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
4. Remove the `id="contactForm"` attribute and the form-note paragraph

## Custom Domain (Optional, later)

If you later want a custom domain (e.g. dedalusmusic.com):
1. Purchase a domain from Namecheap, Google Domains, etc.
2. In your GitHub repo → Settings → Pages → Custom domain
3. Follow GitHub's DNS configuration instructions

## Colors Reference

| Variable         | Value     | Use                        |
|-----------------|-----------|----------------------------|
| --stone          | #0c0b09   | Main background            |
| --parchment      | #c8b89a   | Body text                  |
| --ivory-bright   | #f2eadb   | Headlines                  |
| --gold           | #b8973a   | Accents, links, highlights |
| --gold-dim       | #7a6228   | Subtle gold elements       |
| --rust           | #8b3a2a   | Deep warm accent           |
| --prussian       | #1a2d4a   | Cool shadow tone           |
