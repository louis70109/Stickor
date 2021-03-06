# Stickor

- [ ] Database
- [ ] CSV download
- [ ] Insert sticker queue(or memory)
- [ ] Frontend


# Deployment

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

# Developer Side

## LINE account

- Got A LINE Bot API developer account
  Make sure you already registered, if you need use LINE Bot.

- Go to LINE Developer Console
  - Close auto-reply setting on "Messaging API" Tab.
  - Setup your basic account information. Here is some info you will need to know.
    - Callback URL: `https://{NGROK_URL}/v1/webhooks/line`
    - Verify your webhook.
    - Enable bot join group button.
- You will get following info, need fill back to `.env` file.
  - Channel Secret
  - Channel Access Token (You need to issue one here)

## Localhost

1. first terminal window:

```
pip install -r requirements.txt --user
python api.py
```

2. Created a provisional Https:

```
ngrok http 5000
```

or maybe you have npm environment:

```
npx ngrok http 5000
```

![](https://i.imgur.com/azVdG8j.png)

3. Copied your ngrok url to:
   - `.env` MY_DOMAIN environment property.
   - LINE developer page and `Enabled` join group button:

![](https://i.imgur.com/8jU9CMM.png)

4. Joined bot in your `Group`/`Room`!

# License

MIT License
