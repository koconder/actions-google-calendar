This action runs on a cron and gets a Google calendars events so you can write them to a github repo as JSON. events will be saved in this format in the file you specify in your config (using name as the unique key):

```
{
  "events": [
    {
      "name": "National Public Lands Day",
      "date": "2021-09-25T00:00:00.000Z",
      "description": "It's <b>NPLD</b>"
    }
  ]
}
```

# setup

- create desktop app on google oauth with gcal enabled. create consent screen with your email listed as a test user. download credentials as JSON. run `src/token.js` to generate token.json. set credentials and token json env vars on github action.