# yobbigames.com

The Yobbi Games studio site: Jekyll on GitHub Pages, no theme, no JavaScript framework.
Brand files (logo, colours, banners) come from `marketing/brand/` in the `projects` monorepo;
copy from there, never redraw here.

## Editing

- **Games** live in `_data/games.yml` (one entry per game: name, status, blurb, art, store
  links) plus a short page under `games/<slug>.md` for the longer text. Adding a game is one
  YAML entry and one Markdown file. `hidden: true` keeps a game off the lists until its store
  page is live.
- **Home page** is `_layouts/home.html`; the hero and "Since 2019" text are written there.
- **Legal** pages stay at `/legal/privacy-policy/` and `/legal/terms-of-service/`: the shipped
  apps link to those URLs. `app-ads.txt` and `CNAME` stay as they are.
- `/tiktok/`, `/youtube/`, `/instagram/`, `/x/` and `/facebook/` are copies of the home page
  for bio links, so Cloudflare Web Analytics shows each platform as its own path.
- Analytics: Cloudflare injects Web Analytics at the edge (the domain is proxied); nothing in
  the site code.

## Preview

```bash
bundle install
bundle exec jekyll serve      # http://localhost:4000
```

GitHub Pages builds `main` on push.
