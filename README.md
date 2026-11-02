# Gary J. Hobbins — Author Website (Minimal Edition)

A clean, static website for author **Gary J. Hobbins** and *The Mind's New Liberation, Volume I: The Vow of Honesty*.
Plain HTML, CSS and JavaScript: no frameworks, no build step and no animations.

## Pages
| File | Page | Contents |
|---|---|---|
| `index.html` | Home | Book trailer in the hero, book introduction, three themes, the vision, quote, call to action |
| `about.html` | About | Gary's story, journey timeline, what Gary explains |
| `books.html` | Books | Book details, full synopsis, what's inside, Lesson Plan Directive, full trailer player |
| `contact.html` | Contact | Contact form, contact topics, FAQ |

A **Buy the Book** button is fixed to the right edge of every page (a bottom bar on phones) and links to Amazon:
https://www.amazon.com/ebook/dp/B0HKQ6V7LP/

## Folder structure
```
index.html, about.html, books.html, contact.html
assets/
  css/style.css        all styles (responsive)
  js/main.js           mobile menu, trailer controls, contact form
  video/trailer.mp4    book trailer, web-optimized (1080p H.264/AAC, fast-start)
  img/
    book-cover.jpg / .webp          1600 x 2400 cover
    book-cover-800.jpg / .webp      800 x 1200 cover (used on pages)
    og-image.jpg                    social-sharing preview image
    hero-poster.jpg, scene-*.jpg    stills from the trailer
    favicon.svg
source/
  book-cover-master-1600x2400.png   lossless cover master
```

## View it locally
- **VS Code:** install the "Live Server" extension, right-click `index.html`, then choose **Open with Live Server**.
- **Or in a terminal:** `python -m http.server 8000`, then open http://localhost:8000

## Publish it
Upload the whole folder to any static host (Netlify Drop, Vercel, GitHub Pages, cPanel hosting, etc.).

## Trailer behaviour
- Browsers only allow autoplay with the sound off, so the trailer plays muted on a loop behind the hero text.
- **Pause/Play** and **Sound on/off** buttons sit at the bottom of the hero.
- **Watch with sound** restarts the trailer from the beginning with audio and hides the text overlay.

## Contact form: one setup step
The form validates input, but it needs a destination before it can deliver messages:
1. **Formspree (recommended):** create a free form at formspree.io, then in `contact.html` replace `YOUR_FORM_ID` in the form's `action`.
2. **Or email:** set `data-mailto="name@example.com"` on the `<form>` tag. Submitting then opens the visitor's email app with the message pre-filled.

## About the book cover
The cover image was taken from the full-HD book shot in the trailer, straightened to a flat front view, and enhanced to 1600 x 2400.
For print-perfect sharpness, replace `assets/img/book-cover*.jpg/.webp` with the publisher's original cover file, keeping the same names and the 2:3 proportion.

## Editing
- Colours and fonts are CSS variables at the top of `assets/css/style.css`.
- Fonts: Cormorant Garamond (headings) and Inter (text), loaded from Google Fonts.
