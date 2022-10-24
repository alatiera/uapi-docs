# Static website generation for UAPI group specifications

This repository uses Hugo for static HTML generation.
See https://gohugo.io/getting-started/quick-start/ for a brief intro.

The website uses the [hugo-book](https://github.com/alex-shpak/hugo-book) theme; it is included in this repo as a git submodule.
After cloning this repo please run `git submodule init; git submodule update`.
If you check out a branch or tag, make sure the submodule is up to date by running `git submodule update`.

## Website repo layout

Content resides in the [content](content/) folder.
The top-level README.md is soft-linked to `content/_index.md` and serves as index page.

The repository's [minutes](../minutes) folder is soft-linked to [content/docs/minutes](content/docs/minutes).
New minutes are automatically added to the navigation menu on the left.

New content outside [minutes](../minutes) needs to be manually added to / soft-linked into the `content/` folder to appear on the website.
Content in [content/docs/](content/docs/) will automatically appear in the navigation menu on the left.

## Making changes and testing

You'll need [hugo installed](https://gohugo.io/getting-started/installing/) for rendering changes.

First, make your edits.
Then, start hugo locally (in the repo's `website` directory)to review your changes:

```shell
$ hugo server --minify --disableFastRender
```

Review your changes at http://localhost:1313/docs/ .
