# AI Telegram Group-Chat Summarizer (n8n)
A powerful, no-code/low-code workflow built in n8n that automatically generates a daily AI-powered summary of a Telegram group chat and posts it back to the group.

---

## ✨ Features

- **Automated Daily Execution:** Runs once every 24 hours, completely hands-free.
- **Universal Group Support:** Add the bot to any group, and it will work without any changes.
- **Intelligent Summaries:** Uses Google's Gemini AI to understand conversations and extract key information.
- **Clean, Organized Digests:** The summary includes top conversation topics, shared links, unanswered questions, and the overall chat sentiment.
- **Error-Resistant:** Includes logic to sanitize text for Telegram's formatting rules, preventing common errors.

---

## 🛠️ Tech Stack

- **[n8n.io](https://n8n.io/):** The workflow automation platform used to build and run the bot.
- **[Telegram Bot API](https://core.telegram.org/bots/api):** Used for reading messages from and sending messages to groups.
- **[Google Gemini API](https://ai.google.dev/):** The AI model used for generating the summaries.
- **JavaScript:** Used in `Code` nodes for data manipulation and cleaning.

---

## 🚀 How to Use

1.  **Download the Workflow:** Download the `telegram-digest-workflow.json` file from this repository.
2.  **Import to n8n:** In your n8n instance, go to "Workflows" and click **"Import from File"**. Select the downloaded JSON file.
3.  **Configure Credentials & Token:** You must configure the following nodes with your own credentials and information:
    - **`Get Telegram Messages` Node:** In the URL field, replace `<YOUR_TELEGRAM_TOKEN_HERE>` with your actual Telegram bot token.
    - **`Generate Summary` Node:** Select your Google Gemini API credential from the dropdown.
    - **`Send Summary to Telegram` Node:** Select your Telegram API credential from the dropdown.
4.  **Set Up Your Bot:**
    - Make sure your Telegram bot has **Group Privacy Mode turned OFF** (you can do this via `@BotFather`).
    - Add your bot to any Telegram group you want it to summarize.
5.  **Activate Workflow:** Toggle the workflow to "Active" in the n8n editor.

---
