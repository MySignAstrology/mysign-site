# mysign.app — the landing page

Static marketing site for **My Sign**, served by GitHub Pages straight from
`main`. No build step and no Actions workflow — push and it is live.

Public on purpose, and deliberately separate from the product repo. That one is
private and holds the spec, competitive analysis, safety design and infrastructure
— none of which belongs on a public origin.

## Why this is not the app

GitHub Pages serves static files. My Sign needs a server: model calls, an
ephemeris, a database, sessions, and server-sent events. None of that can run
here, and no amount of client-side work changes it — an API key on a static page
is a published API key.

The app deploys separately (Lambda + DynamoDB, see the product repo). This is the
front door.

## Local

Open `index.html`. There is no build step and no dependencies — one HTML file, an
SVG mark, and two PNGs.

## Brand

`assets/mark.svg` is the source of truth for the mark and is copied from the
product repo's `brand/`. Change it there, not here.
