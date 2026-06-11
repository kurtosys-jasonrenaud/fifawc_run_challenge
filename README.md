# World Cup Run Challenge

A simple dashboard for the Kurtosys team running challenge during FIFA World Cup 2026.

**Live site:** [kurtosys-jasonrenaud.github.io/fifawc_run_challenge](https://kurtosys-jasonrenaud.github.io/fifawc_run_challenge/)

## How it works

Every day, run the total number of goals scored across all World Cup matches from the **previous day**.

- 7 goals yesterday → run 7 km (or miles)
- Run, jog, or walk — any tracker works
- Share a screenshot in the group chat when you're done

## Features

- Fetches yesterday's World Cup scores from ESPN (no API key required)
- Shows total goals and today's run distance
- Lists each match from the previous day with scores
- Toggle between kilometers and miles
- **Share screenshot** — generates a branded image for group chat

## Challenge rules

1. Each day, run the total goals scored across all World Cup matches from the previous day.
2. Run, jog, or walk — any tracker works. Share a screenshot when you're done.
3. Miss a day? Carry the distance over to the next day.
4. Keep it consistent and compete for the leaderboard crown.

## Local development

Open `index.html` in a browser, or serve it locally:

```bash
python3 -m http.server 8080
```

Then visit [http://localhost:8080](http://localhost:8080).

## Deployment

Pushes to `main` automatically deploy the site to GitHub Pages via the `gh-pages` branch.
