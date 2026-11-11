# erodri17.github.io

Source for Elmer Rodriguez's profile site, published at <https://erodri17.github.io>.

Built with Jekyll and the [Klisé](https://github.com/piharpi/jekyll-klise) theme (MIT, see [LICENSE](LICENSE)).

## Where things are

- [`index.md`](index.md) is the home page profile.
- [`about.md`](about.md) is the About page.
- [`_config.yml`](_config.yml) holds the site title, bio line and avatar.
- [`_data/menus.yml`](_data/menus.yml) holds the navigation.
- [`_posts/`](_posts/) holds posts. The Writing link, RSS link and the home page's recent list appear once there is at least one.

## Write a post

Add `_posts/YYYY-MM-DD-title.md`:

    ---
    title: "Post title"
    date: 2026-01-31 09:00:00 -0500
    tags: [powershell]
    ---

## Preview locally

    bundle install
    bundle exec jekyll serve

Then open <http://localhost:4000>.

## Publishing

GitHub Pages builds and publishes the `master` branch.
