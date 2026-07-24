# Security policy

## This project

The World Cup Run Challenge site is a **static** GitHub Pages app. It does not use a backend, database, or API keys for the live dashboard. Scores are loaded from ESPN’s public scoreboard API in the browser.

## What is public

Because the repository and Pages site are public:

- Leaderboard names, distances, and run screenshots are visible to anyone
- Do not commit Strava client secrets, access tokens, `.env` files, or personal API keys
- The Strava helper page (`test.html`) is for local testing only and is not published to GitHub Pages

## Reporting a vulnerability

If you find a security issue (for example an accidentally committed secret, or a way to inject content into the live site):

1. Email the repository owner (do not open a public issue with secret values)
2. Include steps to reproduce and any relevant screenshots (redact secrets)

We will rotate any exposed credentials and fix the issue as quickly as practical.

## Maintainer checklist

- Keep [secret scanning](https://docs.github.com/code-security/secret-scanning) and push protection enabled
- Never paste live Strava client secrets into committed HTML/JS
- Prefer Dependabot updates for GitHub Actions
- Review pull requests before merging to `main` (Pages deploys from `main`)
