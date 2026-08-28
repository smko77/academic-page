# smko77.github.io

Personal academic website for Sangmin Ko, PhD student in mathematics at Columbia University.

**Live site:** https://smko77.github.io

## Running locally

The macOS system Ruby is too old for the gems this site depends on — install Ruby 3.3+ separately and make sure it's first on `PATH` before running any of this.

```bash
brew install ruby
export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"   # or add to your shell profile
bundle install
LANG=en_US.UTF-8 bundle exec jekyll serve --livereload
```

Then open http://localhost:4000. If `jekyll build`/`serve` fails with `Invalid US-ASCII character`, that's a locale issue, not a code issue — `LANG=en_US.UTF-8` above fixes it.

## Structure

Built with [Jekyll](https://jekyllrb.com/) and the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, a fork of [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) (© Michael Rose, MIT License — see [LICENSE](LICENSE)).

- `_pages/` — standalone pages (Home, Research, Teaching, CV, Travel, Seminars index, ...)
- `_seminars/` — seminars organized or co-organized, one file per seminar
- `_data/navigation.yml` — header nav
- `_data/external_seminars.yml` — seminars co-hosted on someone else's site, linked out to from `/seminars/`
- `files/` — CV and other downloadable PDFs
