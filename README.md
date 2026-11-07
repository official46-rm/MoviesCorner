<p align="center">
  <img src="assets/Logo.jpg" alt="Rudra Moviez" width="260">
</p>

<h1 align="center">Rᴜᴅʀᴀ Mᴏᴠɪᴇᴢ Bᴏᴛ</h1>
<p align="center">Telegram Auto Filter • Search • Media Indexing</p>

**Maintainer:** [@RMdveloper4](https://t.me/RMdveloper4)  
**Updates:** [Rudra Movies](https://t.me/RudraMovies4)  
**Support:** [Rudra Moviez](https://t.me/RudraMoviez)  
**Movie catalogue:** [Open channel](https://t.me/+uMyc8ujUr3QzZTZl)  
**Repository:** [https://github.com/official46-rm/MoviesCorner](https://github.com/official46-rm/MoviesCorner)

## Features
- Telegram private-message search and auto-filter
- Indexing of media from configured Telegram channels
- Inline search and pagination
- Optional force-subscribe channel
- Admin commands, logs, and statistics
- MongoDB-backed file and user data

## Deployment (Render)
1. Push the extracted project files (not the ZIP itself) to this repository.
2. In Render, create a **Background Worker** from this GitHub repository.
3. Select **Docker** as the runtime/build method.
4. Add the environment variables listed below in Render.
5. Deploy and inspect the service logs.

Do not expose bot tokens, API hashes, or MongoDB connection strings in GitHub.

## Required environment variables

| Variable | Description |
|---|---|
| `BOT_TOKEN` | Token from Telegram @BotFather |
| `API_ID` | Telegram API ID from `my.telegram.org` |
| `API_HASH` | Telegram API hash from `my.telegram.org` |
| `ADMINS` | Your numeric Telegram user ID |
| `CHANNELS` | Source channel ID(s) to index; separate multiple IDs with spaces |
| `LOG_CHANNEL` | Private log channel ID; make the bot an admin |
| `DATABASE_URI` | MongoDB connection URI |
| `DATABASE_NAME` | Use `RudraMoviez` |

## Optional environment variables

| Variable | Default / purpose |
|---|---|
| `COLLECTION_NAME` | `RudraMoviez_files` |
| `SUPPORT_CHAT` | `RudraMoviez` (username without `@`) |
| `AUTH_CHANNEL` | Optional force-subscribe channel ID |
| `PICS` | Space-separated image URLs for the start screen |
| `INDEX_REQ_CHANNEL` | Defaults to `LOG_CHANNEL` |
| `FILE_STORE_CHANNEL` | Optional file-store channel IDs |
| `AUTO_DELETE_SECONDS` | Auto-delete delay in seconds |
| `IMDB` | `True` or `False` |
| `SPELL_CHECK_REPLY` | `True` or `False` |

## Local run
Use Python 3.10+ where possible, install dependencies, set the environment variables, then run:

```bash
pip install -r requirements.txt
python bot.py
```

The included Dockerfile is used by Render's Docker worker deployment.

## Credits and license
This repository is a customization of the upstream open-source project [AwesomeFilterPro by TamilanBotsZ](https://github.com/TamilanBotsZ/AwesomeFilterPro), which itself includes upstream components and credits. Original license and attribution files are retained. Please review `LICENSE` before redistributing or modifying the project.
