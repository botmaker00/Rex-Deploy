# Rex Deploy – Heroku Deployment via Google Colab

A simple method to deploy your bot to **Heroku** using a **Google Colab notebook**.

---

## 🚀 Deploy Steps

1. Open the Colab notebook:  
   https://colab.research.google.com/github/botmaker00/Rex-Deploy/blob/main/rex_hk_deploy.ipynb

2. Fill these details inside the notebook:
   - HEROKU_API_KEY  
   - HEROKU_APP_NAME  
   - GITHUB_REPO  
   - All required environment variables (BOT_TOKEN, API_ID, API_HASH, DB_URI, etc.)

3. Run all notebook cells.  
   The notebook will:
   - Clone your GitHub repo  
   - Set Heroku config vars  
   - Deploy your bot automatically  

4. After deployment, check Heroku → Activity for "Build succeeded".

---

## 📌 Notes
- Keep your API keys private.  
- Make sure the **Procfile** is correct (example: `worker: python3 main.py`).  
- Re-run the notebook to update/deploy new bot versions.

---

## ✔️ Done!
Your Rex bot is successfully deployed to Heroku using Google Colab.
