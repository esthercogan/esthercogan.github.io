# esthercogan.github.io

Pet Sitting by Esther: a single-page site for Esther Cogan's in-home pet care in Asturias, Spain.

It's plain HTML and CSS with no JavaScript, no build step and no third-party requests. Fonts are self-hosted, and there are no cookies or analytics, so no cookie banner is needed.

## Preview locally

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Publish

Because the repo is named `esthercogan.github.io`, GitHub Pages serves it at <https://esthercogan.github.io/>. If the site doesn't appear after you push to `main`, go to **Settings → Pages** and set **Source** to "Deploy from a branch", with branch `main` and folder `/ (root)`.

## Before launch: fill in the placeholders

Placeholders show on the page with a dashed outline. In `index.html`, search for `TODO(` to find each one.

| What | Where |
| --- | --- |
| WhatsApp number | Replace `34XXXXXXXXX` (digits only, with country code) and `+34 XXX XXX XXX` (as displayed) everywhere |
| Email address | Replace `hello@example.com` everywhere |
| Education & training | The "Education & training" list in the About section |
| Medical and behavior lists | "Expertise" section. Remove anything Esther doesn't offer |
| Legal notice | Footer: NIF and town. Spanish law (LSSI) generally requires this on a business site |

## Fonts

Titles use Tangerine, a calligraphic script. Smaller headings use Cormorant Garamond, and body text uses EB Garamond. Tangerine's capital "I" looks like a "J", so avoid titles that need a capital I (for example "It begins…" reads as "Jt begins…").

## Changing prices

Everything is in the "IV. Rates" section of `index.html`. The daily rate is in the `rate-card` block, and each extra is a `<li>` in a `price-list`. Copy an existing row to add one. Rows without a description simply leave out the `price-list__note` line. If the rates ever change what is included in the daily rate, check the "Included" list too.

## Adding photos

Put image files in `assets/img/photos/`. Portrait-shaped photos (about 4:5) work best in the oval frames. Keep each one under about 300 KB, around 800 × 1000 px.

- **Esther's portrait:** in the About section, replace the `portrait__monogram` span with the `<img>` line shown in the comment above it.
- **Pet gallery ("Familiar faces"):** at the end of the Services section. It currently shows four "Photo to come" placeholders. In each `<li>`, replace the `gallery__placeholder` span with an `<img>` (the comment above the gallery has an example) and fill in the caption. Copy or delete `<li>` rows as needed; four fit per row on desktop and two on phones. Every photo needs a short `alt` description. To hide the gallery until photos arrive, delete it from the `<h3 class="subhead">Familiar faces</h3>` line to the closing `</ul>`.

## Link preview image

`assets/img/og-image.png` is the image WhatsApp and other apps show when the link is shared. If the business name or wording changes, update `tools/og-image.html` and regenerate the image using the command in that file. `tools/touch-icon.html` works the same way for the home-screen icon.

## Files

```text
index.html               the whole page
assets/css/site.css      all styles; colours and textures are at the top
assets/fonts/            Tangerine, Cormorant Garamond and EB Garamond (SIL Open Font License, see OFL.txt)
assets/img/              favicon, home-screen icon, link preview image, photos/
tools/                   sources for the generated images
```
