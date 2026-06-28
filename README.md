# Squad Selection Report — Vercel deploy

`index.html` is the latest generated report, fully self-contained. Player photos load from FIFA's public CDN, so the page needs internet but no build step or server.

`make_report.py` refreshes `index.html` here on every run.

## Deploy options

Drag and drop: open https://vercel.com/new, drop this `deploy` folder, done.

Vercel CLI:

```
cd deploy
vercel        # preview
vercel --prod # production
```

It is a static site. `vercel.json` sets clean URLs and disables caching so each redeploy serves the newest report.

## Notes
- The report links out to FIFA Fantasy (team, league, nations). Those work from any host.
- To publish a new round, regenerate with `make_report.py` and redeploy.
