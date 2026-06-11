# statlean.github.io

GitHub Pages **root site** for the StatLean project, served at
**https://statlean.github.io/**.

This repository contains no source of its own. Its
[`deploy` workflow](.github/workflows/deploy.yml) checks out the source
repository [`StatLean/Stat-Lean`](https://github.com/StatLean/Stat-Lean),
builds:

- the **interactive website** → published at https://statlean.github.io/website/
- the **doc-gen4 API documentation** → published at https://statlean.github.io/docs/

and deploys the combined site to this repo's GitHub Pages.

## Rebuilding

The site rebuilds automatically every night and whenever the deploy workflow
changes. To rebuild on demand after pushing changes to `StatLean/Stat-Lean`,
trigger the workflow manually:

```
gh workflow run deploy.yml --repo StatLean/statlean.github.io
```

or use the **Run workflow** button on the
[Actions tab](https://github.com/StatLean/statlean.github.io/actions/workflows/deploy.yml).
