# RUDRA MOVIEZ BOT

A customized Telegram catalogue/search bot built from the upstream open-source project. The original license and upstream credits are retained in this repository.

> Use this bot only for movies, videos, and other files that you own or are authorized to distribute.

## Branding
- Display name: **Rᴜᴅʀᴀ Mᴏᴠɪᴇᴢ**
- Typography: retained the original small-caps Telegram text style.
- Hosting target: Render or Koyeb (Docker/Python worker).

## Required environment variables
Set these in Render/Koyeb; never commit tokens or database credentials to GitHub.

| Variable | Purpose |
|---|---|
| `BOT_TOKEN` | Token from @BotFather |
| `API_ID` | Telegram API ID from my.telegram.org |
| `API_HASH` | Telegram API hash from my.telegram.org |
| `ADMINS` | Telegram numeric user IDs, space-separated |
| `LOG_CHANNEL` | Private log channel ID; add the bot as admin |
| `DATABASE_URI` | MongoDB connection URI |
| `DATABASE_NAME` | Database name, e.g. `RudraMoviez` |
| `COLLECTION_NAME` | Collection name, e.g. `Rudra_files` |
| `CHANNELS` | Source/catalogue channel IDs, space-separated |
| `AUTH_CHANNEL` | Optional force-subscribe channel ID |
| `SUPPORT_CHAT` | Your support channel/group username, without `@` |
| `OWNER_USERNAME` | Your Telegram username, without `@` |
| `UPDATE_CHANNEL` | Your updates channel username, without `@` |
| `MOVIES_CHANNEL` | Your authorized-content channel username, without `@` |
| `REPO_URL` | Your GitHub repository URL |
| `PICS` | Optional space-separated image URLs for the welcome screen |

## Deploy on Render
1. Push the extracted project folder to your GitHub repository.
2. In Render choose **New + → Background Worker** (or create a Docker service if your account UI offers it).
3. Connect the GitHub repository and choose the branch.
4. Select Docker deployment (the included `Dockerfile`).
5. Add the environment variables listed above.
6. Deploy and inspect the logs.

## Deploy on Koyeb
1. Create an App and choose GitHub as the source.
2. Select this repository and branch.
3. Choose Dockerfile deployment.
4. Add the same environment variables.
5. Deploy and inspect runtime logs.

## Before first launch
- Replace the placeholder Telegram usernames in the environment variables with your real channels.
- Add the bot as admin to the required log/catalogue channels.
- Keep `.env`, tokens, API hashes, and MongoDB credentials out of GitHub.
- Check the upstream license before redistributing modified copies.
