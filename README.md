A bot for automating the submission of daily games to the Lemmy [!dailygames@lemmy.zip](https://lemmy.zip/c/dailygames) community.

## Running

1. Create a file called `.env` in the root directory. It should contain the following fields,
shown with their original values:

```env
LOGIN_INSTANCE_NAME='lemmy.zip'
POST_INSTANCE_NAME='lemmy.zip'
COMMUNITY_NAME='dailygames'
BOT_USERNAME='DailyGameBot'
PASSWORD=''
FEDERATION='local'
TIMEZONE='Australia/Brisbane'
CRON_EXPRESSION='0 0 14 * * *'
```

2. Run `npm i`
3. Run with `npm start`

### Running in Docker

Ensure environment variables as above are set. `docker-compose up` will read from the `.env` file by default, or a different file can be specified with `docker-compose --env-file <filename> up`.

## Testing

1. Add an alternative environment file, `.env.development` with configuration for testing.
2. Run with `npm run dev`
