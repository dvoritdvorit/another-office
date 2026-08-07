# Another Office

Static HTML/CSS rebuild of the Cargo template, ready for GitHub Pages.

## Files

- `index.html` — all page content (nav, upcoming/past events, footer)
- `styles.css` — layout, colors, type
- `fonts/` — drop your ROM Regular files here
- `images/` — drop your background photo here as `hero.jpg`

## Before you publish

1. **Background photo** — add your image to `images/hero.jpg` (any name works,
   just update the `background-image` path in `.bg` in `styles.css`). Until
   then it falls back to a solid sky-blue.

2. **ROM Regular** — this is a paid Dinamo license, so it's not bundled here.
   Add your licensed `.woff2`/`.woff` files to `fonts/`, then uncomment the
   `@font-face` block at the top of `styles.css`. Until then, body text falls
   back to a system sans (Helvetica Neue / Arial).

3. **Instrument Serif** — already wired up via Google Fonts in `index.html`,
   no setup needed.

4. **Real event content** — the event list is still lorem ipsum, matching
   what's live on the Cargo site now. Each event lives in `index.html` as one
   `<li class="event">` block:

   ```html
   <li class="event">
     <div class="event-row">
       <span class="event-date">Mar. 15, 2026</span>
       <a class="event-link" href="#">Ticket link text</a>
     </div>
     <p class="event-title">Event name</p>
     <p class="event-sub">Venue, Year</p>
   </li>
   ```

   For a sold-out / unavailable event (the strikethrough style), use
   `<span class="event-link event-link--sold">` instead of the `<a>`.

5. **Nav links** — `Info` currently scrolls to the footer id (`#info`) and
   `Instagram` points to `instagram.com/cargoworld`. Update the `href`s in
   the `.pill-nav` block in `index.html`.

## Publishing to GitHub Pages

1. Create a new GitHub repo (e.g. `another-office`) and push these files to
   the root of the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`.
4. Save — GitHub will give you a URL like
   `https://yourusername.github.io/another-office/`.
5. For a custom domain, add a `CNAME` file with your domain name to the repo
   root and point your DNS at GitHub's Pages servers (GitHub's docs walk
   through the exact records).

Any edits after that are just: change the HTML/CSS, commit, push — the live
site updates automatically within a minute or two.
