[![Bot Test](https://github.com/Minionguyjpro/Afk-bot/actions/workflows/test.yml/badge.svg)](https://github.com/Minionguyjpro/Afk-bot/actions/workflows/test.yml) [![GitHub package.json version (branch)](https://img.shields.io/github/package-json/v/minionguyjpro/afk-bot/master)](https://github.com/Minionguyjpro/Afk-bot/blob/master/package.json)
# THE GITHUB ACTION SHOULD NOW WORK!
# Afk-bot
A bot to stay AFK on Minecraft servers.
---

### Example Usage
Place the following in for example `/.github/workflows/main.yml`:
```yml
on: push
name: Run the AFK-Bot
jobs:
  join:
    name: Join the server
    runs-on: ubuntu-latest
    steps:
    - name: Start Afk-bot
      uses: Minionguyjpro/Afk-bot@v1.0.3
      with:
        ip: example.ip.org
        name: AFKBOT
        port: 25565
        auto-night-skip: true
```

---

## Settings
Keys can be added directly to your .yml config file or referenced from your project `Secrets` storage.

**Optional**: hide you server by adding secrets. To add a `secret` go to the `Settings` tab in your project then select `Secrets`.
I strongly recommend you store your `ip` and `port` as a secret, in case you want to hide it.

| Key Name                | Required | Example                       | Default Value                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------|----------|-------------------------------|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ip`                | Yes      | `example.ip.org`         | `example.ip.org`                              | Server IP to connect to                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `port`              | No      | `25567`    | `25565`                               | Port for the server to connect, requires an IP                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `name`              | No      | `AFK`    | `afkbot`                              | Name that the bot gets when joining the server                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| `auto-night-skip`                  | No       | `true`                         | `false`                          | Automatically skips the night in the Minecraft server if the bot has permissions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                        |

# All features
- ### Auto Skip Night
Let the bot automatically skip the night if it has permissions.
To enable this, go to config.json file and change 
``auto-night-skip`` from ``false`` to ``true``. If you dont want this anymore you could change it back to ``false``.
- ### 24/7 Aternos server
You can also make an Aternos 24/7 server with this.
Just make a template of this repository, then go to Heroku and make an account if you don't have already. Now create an app on Heroku. Then deploy/connect your repository from Github, then deploy branch. Now start your Aternos server, then go back to Heroku. Now go to Resources and refresh the page. Then enable "worker node index.js".
Now the bot should join the server. It can cost 5-30 seconds. And now go also on the server, now give it creative and put it in an hole underground with torches. Now enjoy your free 24/7 Aternos server!
