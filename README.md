# lguba71.github.io

Professional engineering portfolio website built with **GitHub Pages**, **Jekyll**, and the **Chirpy** theme.

This repository contains the source code and content for the personal engineering portfolio site of **Lajos Guba**.

The site is intended to support professional visibility from LinkedIn and to present practical mechanical engineering experience in a clear, structured, and credible way.

## Purpose of the site

The primary purpose of this website is to act as a focused engineering portfolio for visitors arriving from LinkedIn or other professional channels.

The site is not intended to be a general personal blog. Its main role is to communicate engineering competence, practical project experience, and professional reliability.

The key positioning is:

> Freelance mechanical design engineer with practical experience in production-oriented CAD modelling, fixtures, jigs, manufacturing drawings, DFM support, special-purpose machinery, and production automation.

## Professional focus

The website focuses on the following engineering areas:

* mechanical design engineering,
* production-oriented CAD modelling,
* fixtures, jigs, and manufacturing aids,
* special-purpose machinery,
* manufacturing drawings and technical documentation,
* DFM support,
* production automation experience,
* practical engineering problem solving,
* structured case studies and technical notes.

## Website structure

The site currently includes the following main content areas:

* **Home** — entry point and professional positioning,
* **About** — professional background and engineering profile,
* **Case Studies** — selected engineering examples and project-style summaries,
* **Notes** — shorter technical notes or engineering observations,
* **Posts** — longer articles and blog-style professional content,
* **Categories / Tags / Archives** — standard Jekyll content navigation.

## Repository structure

Important files and folders:

| Path                                 | Purpose                                  |
| ------------------------------------ | ---------------------------------------- |
| `_config.yml`                        | Main Jekyll and Chirpy configuration     |
| `index.html`                         | Homepage entry point                     |
| `_tabs/about.md`                     | About page                               |
| `_tabs/case-studies.md`              | Case studies page                        |
| `_tabs/notes.md`                     | Notes page                               |
| `_posts/`                            | Blog posts and longer technical articles |
| `_data/contact.yml`                  | Contact and social link configuration    |
| `_data/share.yml`                    | Sharing configuration                    |
| `_plugins/posts-lastmod-hook.rb`     | Post last-modified hook                  |
| `.github/workflows/pages-deploy.yml` | GitHub Pages deployment workflow         |
| `Gemfile`                            | Ruby / Jekyll dependency definition      |

## Content direction

The content should support the following visitor path:

1. Understand the professional positioning quickly.
2. See relevant mechanical design and production engineering competence.
3. Find credible examples through case studies or technical posts.
4. Reach the LinkedIn profile or contact channel easily.

The preferred content hierarchy is:

1. engineering portfolio,
2. case studies,
3. mechanical design and automation-related articles,
4. technical notes,
5. selected personal or publication-related links only where they support credibility.

## Editorial principles

Content added to this repository should follow these principles:

* be technically credible,
* avoid exaggerated marketing language,
* focus on practical engineering value,
* avoid unsupported claims,
* clearly separate real experience from general commentary,
* support the professional positioning of the site,
* keep LinkedIn visitors in mind.

## Development notes

This is a Jekyll-based GitHub Pages site using the Chirpy theme structure.

A typical local Jekyll workflow may include:

```bash
bundle install
bundle exec jekyll serve
```

Then open the local development address shown in the terminal.

Actual setup may depend on the installed Ruby, Bundler, Jekyll, and GitHub Pages environment.

## Deployment

The site is deployed through GitHub Pages using the repository workflow configuration under:

```text
.github/workflows/pages-deploy.yml
```

Changes should be reviewed before publishing because the website functions as a public professional portfolio.

## Maintenance priorities

Current improvement priorities:

1. Fix small technical issues in configuration and front matter.
2. Strengthen the LinkedIn visitor path.
3. Improve the About page.
4. Develop the Case Studies section with structured engineering examples.
5. Keep blog content aligned with the professional positioning.
6. Add visual evidence only where it improves credibility and does not expose confidential project details.

## Notes on confidentiality

Engineering examples and case studies should avoid sharing confidential customer data, proprietary drawings, sensitive machine details, or non-public project information.

Where needed, examples should be generalized, anonymized, or recreated as simplified demonstration cases.

## License and reuse

This repository contains a personal professional portfolio website.

The underlying theme and dependencies may have their own licenses. Original written content, case studies, images, and portfolio material should not be reused without permission from the repository owner unless explicitly stated otherwise.
# Chirpy Starter

[![Gem Version](https://img.shields.io/gem/v/jekyll-theme-chirpy)][gem]&nbsp;
[![GitHub license](https://img.shields.io/github/license/cotes2020/chirpy-starter.svg?color=blue)][mit]

A minimal, ready-to-use template for creating a blog with the [**Chirpy**][chirpy] Jekyll theme. Get up and running in minutes with all critical files pre-configured.

## Why This Starter Exists

When installing Chirpy through [RubyGems.org][gem], Jekyll can only read a subset of theme files (`_data`, `_layouts`, `_includes`, `_sass`, `assets`) and limited `_config.yml` options from the gem. As a result, users cannot enjoy the full out-of-the-box experience that Chirpy offers.

To unlock all features, the following files must be present in your Jekyll site:

```shell
.
├── _config.yml
├── _plugins
├── _tabs
└── index.html
```

This starter bundles those files from the latest **Chirpy** release along with a [CD][CD] workflow, so you can start writing immediately.

## Usage

Check out the [theme's docs](https://github.com/cotes2020/jekyll-theme-chirpy/wiki).

## Contributing

This repository is automatically updated with new releases from the theme repository. If you encounter any issues or want to contribute to its improvement, please visit the [theme repository][chirpy] to provide feedback.

## License

This work is published under [MIT][mit] License.

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[CD]: https://en.wikipedia.org/wiki/Continuous_deployment
[mit]: https://github.com/cotes2020/chirpy-starter/blob/master/LICENSE

