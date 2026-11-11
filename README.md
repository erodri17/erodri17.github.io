# erodri17.github.io

Source for Elmer Rodriguez's profile site, live at <https://erodri17.github.io>.

It is a plain Jekyll site with its own templates and one stylesheet. There is no theme and no JavaScript. Pushing to `master` publishes it.

## Common changes

| To change | Edit |
| --- | --- |
| Home page text and the "What I work on" cards | [`index.html`](index.html) |
| About page | [`about.md`](about.md) |
| Name, headline under the name, photo | `author` in [`_config.yml`](_config.yml) |
| Text shown when the site is shared or searched | `description` in [`_config.yml`](_config.yml) |
| Navigation links | [`_data/menus.yml`](_data/menus.yml) |
| Colours and page width | The variables at the top of [`assets/css/style.css`](assets/css/style.css) |
| Browser tab icon | [`assets/favicon.svg`](assets/favicon.svg) |

The photo is [`assets/img/elmeravatar397.jpeg`](assets/img/elmeravatar397.jpeg). To replace it, add the new image to `assets/img/` and point `author.avatar` and `image` in `_config.yml` at it. The photo is cropped to a circle, so a portrait with the face near the top works best.

The stylesheet has two sets of colour variables: light, and dark inside `@media (prefers-color-scheme: dark)`. Visitors get whichever their device is set to. Change a colour in both places.

## Write a post

Add a Markdown file to [`_posts/`](_posts/) named `YYYY-MM-DD-title.md`, for example `_posts/2026-01-31-copying-files-safely.md`:

    ---
    title: "Copying files safely"
    date: 2026-01-31 09:00:00 -0500
    ---

    Post text in Markdown.

The words after the date in the filename become the address, so that example is published at `/copying-files-safely/`.

The site has no posts yet. Once the first one is added, three things appear on their own: the Writing link in the navigation, the "Recent writing" list on the home page and the RSS link in the footer.

## Preview locally

Requires Ruby 3.x with Bundler.

    bundle install
    bundle exec jekyll serve

Then open <http://localhost:4000>. The site rebuilds each time a file is saved, so refresh the browser to see a change. The exception is `_config.yml`: restart the server after editing it.

The [`Gemfile`](Gemfile) is for local preview only. GitHub Pages builds the live site with its own Jekyll version and ignores it, so check the live site after publishing a change to the templates.

## Publish

GitHub Pages builds and publishes the `master` branch. A push is usually live within a minute or two. The build status is under **Actions** in the repository, and a failed build leaves the previous version of the site in place.

If the old version still shows after a successful build, reload with Ctrl+F5 to bypass the browser cache.

## Layout of the repository

- [`_layouts/`](_layouts/): page templates. `default` is the shell every page uses; `home`, `page` and `post` sit inside it.
- [`_includes/`](_includes/): the `<head>`, the header navigation and the footer.
- [`assets/`](assets/): stylesheet, icon and images.
- [`writing.html`](writing.html): the list of all posts, at `/writing/`.
- [`404.html`](404.html): the page shown for a missing address.
