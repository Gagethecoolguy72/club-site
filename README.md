# Black Creek Gun Club — Website

Website for **Black Creek Gun Club**, a private outdoor shooting range in
Hanover County, Virginia (4292 Range Rd, Mechanicsville, VA 23111),
serving local shooters since 1966.

## Features

- **Live social updates** — embedded Facebook page timeline plus quick links
  to both club Facebook pages and Instagram
- **Live open/closed status** — the top bar and hours table compute the club's
  current open/closed state in Eastern time and highlight today's hours
- **Hours & location** — full weekly hours, embedded Google Map, and a
  one-click directions button
- **Ranges** — all six ranges (100 yd, 50 yd, 25 yd, 15 yd, plus two event ranges)
- **Membership pricing** — individual ($350/yr), family add-on ($100/yr),
  and guest pass ($30/day) cards with NRA/safety-briefing requirements
- **Matches & events, range rules, and FAQ** sections
- Fully responsive, no build step — a single `index.html`

## Running locally

Just open `index.html` in a browser, or serve it:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

> Note: the Facebook and Google Maps embeds require an internet connection.

## Deploying

This is a static site — it works as-is on GitHub Pages, Netlify, Vercel, or
any web host. For GitHub Pages: Settings → Pages → deploy from branch, root folder.

## Updating club info

- **Hours** — edit the table in the `#hours` section *and* the `hours` object
  in the script at the bottom of `index.html` (day `0` = Sunday, 24-hour values).
- **Contact info** — search for the phone/email strings and replace throughout.
- **Social feeds** — the Facebook embed URL is in the `#updates` section
  (`plugins/page.php?href=...`); point it at whichever page the club actively posts on.
