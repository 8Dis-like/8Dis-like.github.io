# Zagho's Blog

Personal blog of Zagho, built with [Hexo](https://hexo.io/) and the
[Matery](https://github.com/blinkfox/hexo-theme-matery) theme.

The published site is available at:

<https://8Dis-like.github.io>

## Features

- Markdown-based posts stored in [`source/_posts/`](source/_posts/)
- Chinese and English content
- Custom post URLs generated with `hexo-abbrlink`
- Categories, tags, archives, search, and RSS-friendly static pages
- Giscus comments backed by GitHub Discussions
- GitHub Pages deployment through `hexo-deployer-git`

## Requirements

- Node.js 18 or newer
- npm

## Getting started

Install dependencies:

```bash
npm install
```

Generate the static site:

```bash
npm run build
```

Start a local preview server:

```bash
npm run server
```

The local site is served at <http://localhost:4000>.

## Writing a post

Create a new post with:

```bash
npx hexo new post "Post title"
```

Posts are written in Markdown and placed in [`source/_posts/`](source/_posts/).
The post front matter controls the title, date, categories, tags, cover image,
and stable `abbrlink` used in the published URL.

## Deployment

The production site is deployed to the `main` branch of
[`8Dis-like/8Dis-like.github.io`](https://github.com/8Dis-like/8Dis-like.github.io)
with:

```bash
npm run clean
npm run build
npm run deploy
```

The deploy command uses the Git remote configured in [`_config.yml`](_config.yml).
Do not use `sudo` for Hexo commands; generated files should remain owned by the
current user.

## Project layout

```text
source/_posts/       Markdown blog posts
source/medias/       Images and other post assets
themes/matery/       Active theme and site customizations
_config.yml          Hexo site configuration
package.json         Development and deployment scripts
```

## Comments

Comments are provided by Giscus. The configuration is in
[`themes/matery/_config.yml`](themes/matery/_config.yml), and the post-level
embed is rendered by
[`themes/matery/layout/_partial/giscus.ejs`](themes/matery/layout/_partial/giscus.ejs).
Each post uses a stable identifier for its Giscus discussion so comments do not
move between articles when the site is regenerated.
