# Economic_bot prototype

This bot fetches **economic news** (TradingEconomics, Investing, ForexFactory, Econoday),  
classifies them into **Short Term** vs **Long Term**, and generates **automatic Bullish/Bearish conclusions**.  
It then posts updates into **Telegram**.

---

## 🔹 Setup

1. **Create Telegram Bot**
   - In Telegram, talk to `@BotFather`
   - `/newbot` → choose name + username
   - Save the **API Token**

2. **Get Chat ID**
   - Add bot to your channel/group (as Admin if channel)
   - Send a message there
   - Visit:  
     ```
     https://api.telegram.org/bot<YOUR_TOKEN>/getUpdates
     ```
   - Copy the `chat.id` (looks like `-1001234567890`)

3. **Environment Variables**
   - `TELEGRAM_TOKEN` = your Bot token
   - `TELEGRAM_CHAT_ID` = your channel/group id
   - `TE_CREDENTIAL` = `guest:guest` or your TradingEconomics API key

---

## 🔹 Run Locally
```bash
pip install -r requirements.txt
export TELEGRAM_TOKEN=123456:ABC...
export TELEGRAM_CHAT_ID=-1001234567890
python economic_bot.py
