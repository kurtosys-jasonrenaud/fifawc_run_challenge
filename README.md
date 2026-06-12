# World Cup Run Challenge

A simple dashboard for the Kurtosys team running challenge during FIFA World Cup 2026.

**Live site:** [kurtosys-jasonrenaud.github.io/fifawc_run_challenge](https://kurtosys-jasonrenaud.github.io/fifawc_run_challenge/)

## How it works

Every day, run the total number of goals scored across all World Cup matches from the **previous day**.

- 7 goals yesterday → run 7 km (or miles)
- Run, jog, or walk. Any tracker works
- Share a screenshot in the group chat when you're done

Matches are counted by **local kickoff date**, so early-morning games are grouped with the correct calendar day.

## Features

- Fetches yesterday's World Cup scores from ESPN (no API key required)
- Animated daily goal reveal and today's fixture preview
- Carry-over calculator for missed days (saved in your browser)
- Shows total goals and today's run distance
- Lists each match from the previous day with scores
- Toggle between kilometers and miles
- **Copy for chat**: one-tap message for WhatsApp or Slack
- **Share screenshot**: generates a branded image for group chat
- **Team leaderboard**: loaded from `leaderboard.json` with stats and badges

## Leaderboard

Runner data is stored in [`leaderboard.json`](leaderboard.json). Each morning, share tracker screenshots in the group chat and the leaderboard can be updated from those.

### Data format

```json
{
  "updated": "2026-06-12",
  "defaultUnit": "km",
  "runners": [
    {
      "name": "Alex Runner",
      "runs": [
        {
          "date": "2026-06-12",
          "matchDayGoals": 2,
          "distance": 2,
          "unit": "km",
          "completed": true
        }
      ]
    }
  ]
}
```

- `date`: the day the run was completed (YYYY-MM-DD)
- `matchDayGoals`: goals from the previous day's matches
- `distance`: distance run that day
- `completed`: `true` when the run counts toward the leaderboard

The site ranks runners by total distance, then streak.

## Challenge rules

1. Each day, run the total goals scored across all World Cup matches from the previous day.
2. Run, jog, or walk. Any tracker works. Share a screenshot when you're done.
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
