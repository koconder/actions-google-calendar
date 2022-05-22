# Google Calendar Actions 

## Description

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

## Setup

- Head to Google Cloud project new or existing
- Sidebar select `API and services`
- Click `Library` and enable `Google Calendar API`
- Click `OAuth consent screen` as `External`
- Create consent screen with your email(s) listed as a test user(s).
- Download credentials as JSON and sabe in root as `credentials.json`.
- Run `node src/token.js` to generate token.json following the prompts. When you get redirected in browser the string afer `code=` is your token.
- Set credentials and token json env vars on github action using the output from the script.

## Todo

- Add support for multiple calendars.
- Add support for filtering events by date.
- Add support for filtering events by name.
- Add support for other output formats including markdown, txt, csv.
