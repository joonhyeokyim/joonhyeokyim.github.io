# Joon-Hyeok Yim's website

Source for <https://joonhyeokyim.github.io/>, built with Jekyll and the
[Academic theme](https://github.com/LeNPaul/academic) by Paul Le.

The site keeps its original Home, Papers, Research, CV, and Contact structure,
portrait, and social links. Content is stored in Markdown and YAML; there is
no database or additional JavaScript framework.

## Preview locally

With Ruby 3.3 and Bundler installed (the current dependency set was verified
with Ruby 3.3):

```sh
bundle install
bundle exec jekyll serve
```

Open <http://localhost:4000>. For a production build:

```sh
JEKYLL_ENV=production bundle exec jekyll build
```

The generated site is written to `_site/`. Do not commit that directory.
Continue using the repository's existing GitHub Pages publishing settings.
