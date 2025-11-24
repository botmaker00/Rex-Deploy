# Rex Deploy – Heroku Deployment via Google Colab

A simple method to deploy your **Encoding Bot** to **Heroku** using a **Google Colab notebook**.

---

## 🚀 Deploy Steps

1. Open the Colab notebook:  
   https://colab.research.google.com/github/botmaker00/Rex-Deploy/blob/main/rex_hk_deploy.ipynb

2. Follow the notebook cells in order:
   - **Step 1:** Login with Heroku email and API key
   - **Step 2:** (Optional) Create new Heroku apps
   - **Step 3:** Configure your bot by choosing one of three methods:
     - **Manual**: Fill form fields directly in Colab
     - **Gist URL**: Provide a raw GitHub Gist link to your `config.env`
     - **Upload File**: Upload a pre-made `config.env` file
   - **Step 4:** Deploy all configured apps to Heroku

3. The notebook will:
   - Clone the Rex-Deploy repository  
   - Create a properly formatted `config.env` file in each app folder
   - Push the app to Heroku with all configurations

4. After deployment, your bot will automatically load settings from `config.env` at runtime.

---

## 📋 Required Configuration Variables

The bot requires these environment variables (all set in `config.env`):

### Required:
- `API_ID` - Your Telegram API ID (integer)
- `API_HASH` - Your Telegram API Hash (string)
- `BOT_TOKEN` - Your Telegram Bot Token (from @BotFather)
- `OWNER_ID` - Your Telegram User ID (integer)
- `LOG_CHANNEL` - Channel ID for logging (integer, e.g., -1001234567890)
- `MONGO_URI` - MongoDB connection string
- `SESSION_NAME` - Bot session name (default: "encoderbot")

### Optional:
- `SUDO_USERS` - Comma-separated user IDs with sudo access
- `EVERYONE_CHATS` - Comma-separated chat IDs where everyone can use the bot
- `DOWNLOAD_DIR` - Download directory path (default: "VideoEncoder/downloads/")
- `ENCODE_DIR` - Encode directory path (default: "VideoEncoder/encodes/")
- `INDEX_URL` - Your index URL for file sharing
- `DRIVE_DIR` - Google Drive directory path
- `UPSTREAM_REPO` - Repository URL for auto-updates
- `UPSTREAM_BRANCH` - Branch name for auto-updates (default: "main")

---

## 📌 Important Notes

- **Config Loading:** The bot uses `python-dotenv` to load `config.env` at runtime. The file must be in the app root directory.
- **Config Format:** The notebook automatically generates a properly formatted `.env` file (key=value, no spaces).
- **Security:** Keep your API keys and tokens private. Never share your `config.env` publicly.
- **Updates:** Re-run the notebook to update your bot or change configurations.
- **Config Vars:** By default, configs are stored in `config.env`. Optionally, you can also set Heroku Config Vars using the provided helper cell.

---

## 🔧 Troubleshooting

- **Bot not starting?** Check Heroku logs (Step 5 in notebook)
- **Missing config error?** Ensure all required variables are filled in Step 3
- **Deploy failed?** Verify your Heroku app name is correct and you have sufficient dyno hours

---

## ✔️ Done!
Your Encoding Bot is successfully deployed to Heroku using Google Colab and will load configurations from `config.env`.
