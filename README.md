# Catharina Behrens — academic website

An academic website built with [al-folio](https://github.com/alshedivat/al-folio), using its versioned Jekyll theme and plugin gems.

## Update your website

| Content                      | File                       |
| ---------------------------- | -------------------------- |
| Biography and homepage       | `_pages/about.md`          |
| Research and working papers  | `_pages/research.md`       |
| Publications (BibTeX)        | `_bibliography/papers.bib` |
| Publications page            | `_pages/publications.md`   |
| CV and PDF link              | `_pages/cv.md`             |
| Social and contact links     | `_data/socials.yml`        |
| Name, URL, and theme options | `_config.yml`              |

To add a portrait, upload it to `assets/img/` and set `profile.image` in `_pages/about.md` to its filename.

The initial biography, education, research interests, and CV link are based on the [RFBerlin staff profile](https://www.rfberlin.com/staff/catharina-behren/). Confirm these details when personalizing the site. No sample papers or invented contact details are included.

## Publishing

In **Settings → Pages → Build and deployment**, select **GitHub Actions** as the source. The workflow builds pull requests and publishes pushes to `main`.

## Local preview

With Ruby 3.3.5 and Node.js installed:

```sh
bundle install
npm ci
bundle exec jekyll serve --baseurl ""
```

Open `http://localhost:4000/`. The personal site's `baseurl` is empty because it is hosted at the root of `catharinabehrens.github.io`.

## Validation

```sh
npm run lint:prettier
bundle exec al-folio upgrade audit --no-fail
bundle exec jekyll build --baseurl ""
```

Theme source: al-folio upstream commit `8158dd07b40eda745da47a55a8a711332286dbf5`. The upstream MIT license is retained in `LICENSE`. Theme runtime files are supplied by the pinned gems; no local runtime overrides are used.
