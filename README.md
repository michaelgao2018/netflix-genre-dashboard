# Netflix Genre Insight Dashboard

A single self-contained HTML page. Every one of the 14,903 Netflix titles with
≥1M views is embedded in the file, so the page needs no API, no database and no
build step — open it and it works.

## Deploying

This is a static site with `index.html` at the repository root. Vercel detects
that automatically: no framework preset, no build command, no output directory.

## What's in it

- Filters: content type, report period, genre (11 labels), label confidence,
  and a typeahead multi-select title picker
- Two grains: per-season rows, or seasons rolled up by show
- Two metrics: views, or hours viewed
- Genre leaderboard (total / median per title / title count), per-title
  distribution with quartiles, Film-vs-TV split, and movement across report periods
- Sortable genre and title tables, both exporting to CSV

## Data caveats baked into the page

- The source column named "Release Year" is the **engagement report period**,
  not a release year. It is labelled Report period throughout.
- The 2023 period carries ~3x the titles of later periods, so period totals are
  not comparable — use shares and per-title medians.
- Views = hours ÷ runtime, which structurally favours short content. Kids &
  Family Animation leads on views; Romance / Drama and Crime / Thriller lead on
  hours watched.
