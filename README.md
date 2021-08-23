# Starred

[![ci](https://github.com/maguowei/starred/actions/workflows/ci.yml/badge.svg)](https://github.com/maguowei/starred/actions/workflows/ci.yml)
[![Upload Python Package](https://github.com/maguowei/starred/actions/workflows/deploy.yml/badge.svg)](https://github.com/maguowei/starred/actions/workflows/deploy.yml)

## Install

```bash

$ pip install git+https://github.com/ntk148v/starred.git
$ starred --username ntk148v --sort > README.md
```

## Usage

```bash
$ starred --help

$ starred --help

Usage: starred [OPTIONS]

    GitHub starred

    creating your own Awesome List used GitHub stars!

    example:     starred --username ntk148v --sort > README.md

Options:
    --username TEXT        GitHub username
    --token TEXT           GitHub token
    --sort                 sort by language
    --repository TEXT      repository name
    --message TEXT         commit message
    --format [table|list]  output repository information format. Table by default.
    --version              Show the version and exit.\
    --help                 Show this message and exit.
```

## Demo

```bash
# automatically create the repository
$ export GITHUB_TOKEN=yourtoken
$ starred --username yourname --repository awesome-stars --sort
```

- [`ntk148v/awesome-stars`](https://github.com/ntk148v/awesome-stars)
- [update awesome-stars every day by GitHub Action](https://github.com/ntk148v/awesome-stars/blob/master/.github/workflows/schedules.yml) the example with GitHub Action

## FAQ

1. Generate new token

   link: [Github Personal access tokens](https://github.com/settings/tokens)

2. Why do I need a token?

   - For unauthenticated requests, the rate limit is 60 requests per
     hour.
     see [Github Api Rate
     Limiting](https://developer.github.com/v3/#rate-limiting)
   - The token must be passed together when you want to automatically
     create the repository.

3. Install the master branch version

   ```bash
   $ pip install -e git+https://github.com/ntk148v/starred#egg=starred
   ```
