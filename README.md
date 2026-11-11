# erodri17.github.io

Source for Elmer Rodriguez's profile site, published at <https://erodri17.github.io>.

A plain Jekyll site with its own layouts and one stylesheet. No theme and no JavaScript.

## Where things are

- [`index.html`](index.html) is the home page: intro, what I work on, selected tools, contact.
- [`about.md`](about.md) is the About page.
- [`_config.yml`](_config.yml) holds the site title, headline and photo.
- [`_data/menus.yml`](_data/menus.yml) holds the navigation.
- [`_layouts/`](_layouts/) and [`_includes/`](_includes/) hold the page templates.
- [`assets/css/style.css`](assets/css/style.css) holds all styling. Colours are the variables at the top; dark mode follows the visitor's device setting.
- [`_posts/`](_posts/) holds posts. The Writing link, RSS link and the home page's recent list appear once there is at least one.

## Write a post

Add `_posts/YYYY-MM-DD-title.md`:

    ---
    title: "Post title"
    date: 2026-01-31 09:00:00 -0500
    ---

## Preview locally

    bundle install
    bundle exec jekyll serve

Then open <http://localhost:4000>.

## Publishing

GitHub Pages builds and publishes the `master` branch.
