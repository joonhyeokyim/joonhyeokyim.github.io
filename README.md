# Joon-Hyeok Yim's academic website

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

## Update content

| Content | Source |
| --- | --- |
| Name, short description, canonical site URL | `_config.yml` |
| Homepage biography | `index.md` |
| Papers, author order, venues, and links | `_data/papers.yml` |
| Research overview | `research.md` and `_data/settings.yml` |
| Individual research topics | `research/hyp-tree-spaces.md`, `research/random-graphs.md`, `research/ultrametric-apps.md` |
| CV section order | `_data/cv/sections.yml` |
| Education, experience, teaching, and honors | Corresponding files in `_data/cv/` |
| Downloadable CV | `assets/JoonHyeokYim-CV.pdf` |
| Email and social links | `_data/settings.yml` |
| Portrait | `assets/img/myself.jpg` |
| Styling | `_sass/site.scss` |

Each paper is listed once in `_data/papers.yml`. Set `featured: true` to show
it on the homepage as well as the Papers page. Add links as `label` / `url`
pairs. Local asset links should start with `/`; the templates respect the
site's `baseurl` setting.

Contact title, department, institution, and address are optional. The draft
retains the existing publicly listed Yale email; confirm or replace it before
publishing if that address is no longer preferred. The downloadable CV is the
original supplied PDF, so update it separately when a newer CV is available.

## Content sources

The refresh uses existing public material:

- [NeurIPS 2023 paper / arXiv record](https://arxiv.org/abs/2409.01010).
- [Hyperbolicity, slimness, and minsize, on average](https://arxiv.org/abs/2412.05746).
- [Yale dissertation record](https://elischolar.library.yale.edu/gsas_dissertations/1606/).
- The existing `assets/JoonHyeokYim-CV.pdf` for education, past appointment,
  teaching, and honors.

The NeurIPS paper was published in 2023 and posted to arXiv in 2024. The site
uses the conference year. Current affiliation is left unspecified; unpublished
projects are not listed.

The old theme's sample courses, posts, and unused People page remain in the
source but are excluded from the build in `_config.yml`. Only `index.md`
provides the homepage. The theme's MIT license is retained in `LICENSE.txt`.
