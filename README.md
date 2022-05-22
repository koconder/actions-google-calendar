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

- Create desktop app on google oauth with gcal enabled.
- Create consent screen with your email listed as a test user.
- Download credentials as JSON. run `src/token.js` to generate token.json.
- Set credentials and token json env vars on github action.

## Todo

- Add support for multiple calendars.
- Add support for filtering events by date.
- Add support for filtering events by name.
- Add support for other output formats including markdown, txt, csv.
