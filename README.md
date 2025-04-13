
# VaaniXUserbot

**VaaniXUserbot** is a powerful Telegram spam userbot built using the Telethon library. This bot supports multi-account spamming, reply raids, and many custom commands. You can control it from your main Telegram account and manage up to 10 userbot sessions.

<p align="center">
  <img src="https://telegra.ph/file/fc22cb568f8e82f574109.jpg" alt="VaaniXUserbot SPAM BOT">
</p>

---

## Features

- `.ping` – Check if the bot is active
- `.alive` – Check bot status
- `.help` – List all available commands
- `.id` – Get your Telegram user ID
- `.userinfo` – Get detailed user info
- `.startraid [username] [count]` – Spam a user/group multiple times
- `.stopraid` – Stop ongoing spam
- `.startreply [reply text]` – Start replying to a message repeatedly
- `.stopreply` – Stop replying
- `.replyraid` – Reply to a message multiple times
- `.restart` – Restart the bot

---

## Mandatory Environment Variables

| Variable Name | Description |
|---------------|-------------|
| `API_ID`      | Telegram API ID from https://my.telegram.org |
| `API_HASH`    | Telegram API Hash from https://my.telegram.org |
| `STRING_SESSION` | String session of your Telegram account (generate using script) |
| `SUDO_USERS`  | Telegram user IDs of admins (space separated) |
| `BIO_MESSAGE` | Message to be set in bio (optional) |

---


## How to Generate a String Session (Manual Termux Method)

1. **Install Telethon in Termux**:
    ```bash
    pkg update && pkg upgrade -y
    pkg install python -y
    pip install telethon
    ```

2. **Create string session script**:
    ```bash
    nano generate_string.py
    ```

    Paste the following code:
    ```python
    from telethon.sync import TelegramClient
    from telethon.sessions import StringSession

    api_id = int(input("Enter your API ID: "))
    api_hash = input("Enter your API HASH: ")

    with TelegramClient(StringSession(), api_id, api_hash) as client:
        print("
✅ Your String Session:
")
        print(client.session.save())
        print("
� ️ Keep this string safe and do not share it with anyone.")
    ```

3. **Run the script**:
    ```bash
    python generate_string.py
    ```

4. Enter your **API ID**, **API HASH**, and verify your number & OTP. The string session will be displayed.


---

## How to Deploy (Termux)

1. Install Termux from F-Droid or Play Store  
2. Run the following commands:

```bash
pkg update && pkg upgrade -y
pkg install python git unzip -y
pip install telethon python-dotenv
termux-setup-storage
cd /sdcard/Download
unzip Vaani_Userbot.zip -d Userbot
cd Userbot
python Vaanibot.py
```

---

## Support

For issues or suggestions, contact:

- Telegram Channel: [@VaaniXUserbot_OFFICIAL](https://t.me/VaaniXuserbot_Official)
- Support Group: [@VaaniXUserbot_OFFICIALCHAT](https://t.me/VaaniXUserbot_OFFICIALCHAT)
- Feedback Bot: [@VaaniXUserbot_feedbackbot](https://t.me/VaaniXUserbot_feedbackbot)

---

## Credits

- [Team VaaniX](https://t.me/VaaniXUserbot_OFFICIAL)
- Telethon Team
- Contributors from ThorXops, VaaniX Team

---

## License

This bot is open-source and for educational purposes only. Use it responsibly.
