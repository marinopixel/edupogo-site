[README.md](https://github.com/user-attachments/files/32876526/README.md)
# edupogo.com

The website for **Edupogo — Learn with Pogo**, a learning app for children
aged 4 to 14. Pogo, a friendly dinosaur, explains *how* and *why* things
work instead of handing over answers.

**Live site:** [edupogo.com](https://edupogo.com) ·
**App Store:** [Edupogo — Learn with Pogo](https://apps.apple.com/app/edupogo-learn-with-pogo/id6770953993)

---

## What's in here

| File | What it is |
|---|---|
| `index.html` | Home page |
| `privacy.html` | Privacy policy |
| `terms.html` | Terms of use |

Three files. That's the whole site.

## No build step, and no dependencies

Each page is **completely self-contained**: the stylesheet lives in a
`<style>` block inside the file, and the images are embedded as data URIs.
Open any of them straight from your desktop and it renders exactly as it
does on the live site.

That makes the files larger than they'd otherwise be — around 500 KB each,
mostly the illustration. It's a deliberate trade. A brochure site with
three pages gains very little from a build pipeline, and loses a lot the
first time a stylesheet goes missing and the page renders as plain text.
Nothing here can break because a file didn't come along.

The only thing loaded from outside is the typefaces, from Google Fonts.

## Changing something

No tooling required.

1. Click the file above, then the pencil icon
2. Edit, then **Commit changes**
3. GitHub Pages redeploys on its own, usually within a minute

To change an image, edit the file locally, re-encode it as a data URI, and
re-upload the page.

## How it's put together

**Typefaces** — Fredoka for headings, Nunito for body text. The same pair
the app uses, so the site and the product look like one thing.

**Colour** — the ten subject pills use the exact colours from the app's own
theme. Math is the same teal on the website as it is on a child's phone.

**The wordmark** — each letter is a different colour with a dark outline.
The outline isn't decoration: without it, the yellow `u` would be
unreadable on white, which is why bright yellow usually gets quietly
muddied into amber on light backgrounds.

**Accessibility** — the site follows the same rules as the app. Colour is
never the only thing carrying meaning, contrast is checked against WCAG AA,
`prefers-reduced-motion` stops every animation, and the layout reflows to a
single column at phone width. The app itself carries six of Apple's
accessibility labels: VoiceOver, Voice Control, Larger Text, Sufficient
Contrast, Differentiate Without Colour Alone and Reduced Motion.

**Dark mode** — every colour is a token redefined under
`prefers-color-scheme: dark`.

## Related

- `edupogo-backend` — the API that answers children's questions (private)
- The Flutter app itself lives in a separate project

## Contact

[support@edupogo.com](mailto:support@edupogo.com) ·
[privacy@edupogo.com](mailto:privacy@edupogo.com)

© Edupogo LLC · Miami, FL
