A Discord bot that renames a Discord channel based on Google Calendar meetings.

### Features
- Automatic keyword extraction using RAKE
- Supports a single voice or text channel

### Installation
Environment variables to set (`.env` files also supported):

- `DISCORD_TOKEN`: The Discord app token
- `CALENDAR_ID`: The Google calendar ID. Found explicitly on the calendar's settings page.
- `DISCORD_CHANNEL`: The Discord channel ID. Right click on a Discord channel and select `COPY_ID`.
- `REFRESH_INTERVAL`: How often to refresh via Google calendar. Defaults to 30 minutes if unspecified.

Also, you need to create a Google Cloud Platform project with a
`credentials.json` file in the directory.
Press _Enable the Google Calendar API_ and download `credentials.json`,
as seen on [Google's Node.js Quickstart](https://developers.google.com/calendar/quickstart/nodejs).

After that, you can install all the required dependencies using `npm` or `yarn`:
```
npm install
```

Note that you need to run the bot at least one, in order to confirm access to your Google Calendar:
```
node dlablord.js
```
After that, the `token.json` file will be automatically created in the plugin's directory, containing
the credentials of the current Google Drive user.

### Developing
```
nodemon --inspect dlablord.js
```
