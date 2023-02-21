# SuchABot
A discord bot originally made by Tomato#6966. He discontinued his Milrato bot so I am picking up what he made and making it better.

# Public Bot!
 
[**Invite the Public Version of this Bot**](https://dsc.gg/suchabot) so you don't need to host it by yourself or [join my Discord server](https://dsc.gg/dscdev) to get a custom Bot hosted for you! (SOON!)


# Important notes and thank ❤️
First of all, thanks for using this Source Code, it was and is a ton of work to maintain it!
That's why I'm asking everyone to join my [Discord Server](https://dsc.gg/dscdev)!

# Installation Guide 🔥

## ✅ Hosting Requirements

<details>
  <summary>Click to expand</summary>

  * [nodejs](https://nodejs.org) version 16.6 or higher, I recommend the latest STABLE version
  * [python](https://python.org) version 3.8 or higher, to install the database `enmap` (better-sqlite3)

</details>

## 🤖 Bot Requirements

<details>
  <summary>Click to expand</summary>
 
  1. Download the [Source Code](https://github.com/wbrous/SuchABot/)
     * Either by: `git clone https://github.com/Tomato6966/Multipurpose-discord-bot`
  
</details>

## 🎶 Music Requirements

<details>
  <summary>Click to expand</summary>

  *To allow your Bot to play music, you need to connect it to a LavaLink station!*
  *There are many public ones out there for example lava.link*
  An example for a public configuration will be listed down below.
   
  1. Make sure `Java 11` is installed on your system!
     * [Click here for a Download for **Linux**](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/3.5.2-java-11)
     * [Click here for a Download for **Windows**](https://downloads.milrato.eu/windows/java/jdk-11.0.11.exe) ​
  2. Download [Lavalink.jar](https://github.com/freyacodes/Lavalink/releases/download/3.4/Lavalink.jar)
     * Here is a direct link: https://github.com/freyacodes/Lavalink/releases/download/3.4/Lavalink.jar
     * If you are on linux do this: `wget https://github.com/freyacodes/Lavalink/releases/download/3.4/Lavalink.jar` (prep: `apt-get install -y wget`)
  3. Download [application.yml](https://cdn.discordapp.com/attachments/734517910025928765/934084553751015475/application.yml)
     * Download my example, it's the configuration for the lavalink.jar file!
  4. Now put application.yml and Lavalink.jar in the same folder and start it
     * To start LavaLink type: `java -jar Lavalink.jar`
     * Make sure to keep your terminal Open!
     * If you want to use something like `npm i -g pm2` to host it without keeping your terminal open type: `pm2 start java -- -jar Lavalink.jar`
  5. The settings like **password** in application.yml and **port** must be provided in the `botconfig/config.json` of the Bot
     * If you used the default settings, than no adjustments are needed and it should look like this: 
     ```json
     {
        "clientsettings": {
            "nodes": [
                {
                    "host": "localhost",
                    "port": 2333,
                    "password": "youshallnotpass"
                }
            ]
        }
     }
     ```
  6. You don't want to host your own LavaLink?
     * [Here is a list of many free-to-use LavaLink Servers!](https://lavalink.darrennathanael.com/#how2host)
     * Or just use something like this: 
     ```json
     {
        "clientsettings": {
            "nodes": [
                {
                    "host": "lava.link",
                    "port": 80,
                    "password": "Anything for the Password"
                }
            ]
        }
     }
     ```

</details>

## 🤖 Configuration and Starting

<details>
  <summary>Click to expand</summary>

  **NOTE:** *You can do the exact same configuration inside of the `example.env` file, just make sure to rename it to `.env` or use environment variables!*
 
   1. Check `🎶 Music Requirements` that you started lavalink / use a valid public lavalink station.
   2. Fill in all required data in `./botconfig/config.json` **NOTE:** *If you're on replit.com, it is exposed to everyone!(use .env instead)*
   3. Fill in all required data in the `.json` files in `./social_log/` (`./social_log/streamconfig.json` & `./social_log/twitter.json`), if you want the SOCIAL LOGS to work! (the key `authToken` in streamconfig does not need to be filled in!)
   4. You can adjust some settings in the other `./botconfig/*.json` Files, **BUT PLEASE __KEEP__ MY CREDITS & ADS!** This is the only way on how my hard work is "revenued".
   5. Now start the bot by opening a cmd line in that folder and typing: `node index.js` or `npm start`
     * If you don't want to keep the terminal open or if you're on linux, check out [pm2 (and my tutorial)](https://github.com/Tomato6966/Debian-Cheat-Sheet-Setup/wiki/4-pm2-tutorial) and type: `pm2 start --name Bot_Name index.js`
  
</details>

## ❓ Where to get which Api-Key(s)

<details>
  <summary>Click to expand</summary>

  **NOTE:** *You can do the exact same configuration inside of the `example.env` file, just make sure to rename it to `.env` or use environment variables!*
 
  1. `./botconfig/config.json`
     * `token` you can get from: [discord-Developers](https://discord.com/developers/applications)
     * `memer_api` you can get from: [Meme-Development DC](https://discord.gg/Mc2FudJkgP) `DONE FOR YOU`
     * `spotify.clientSecret` you can get from: [Spotify-Developer](https://developer.spotify.com) `DONE FOR YOU`
     * `spotify.clientID` you can get from: [Spotify-Developer](https://developer.spotify.com) `DONE FOR YOU`
     * `fnbr` is a FNBR token, which you may get from [FNBRO.co](https://fnbr.co/api/docs) (needed for fnshop) `DONE FOR YOU`
     * `fortnitetracker` is a FORTNITE TRACKER token, which you may get from [fortnitetracker.com](https://fortnitetracker.com/site-api) (needed for fnstats) `DONE FOR YOU`
  2. `./social_log/streamconfig.json`
     * `twitch_clientID` you can get from: [Twitch-Developer](https://dev.twitch.tv/docs/api) ([developer-console](https://dev.twitch.tv/console)) `DONE FOR YOU`
     * `twitch_secret` you can get from: [Twitch-Developer](https://dev.twitch.tv/docs/api) ([developer-console](https://dev.twitch.tv/console)) `DONE FOR YOU`
     * `authToken` is not required to be filled in --> will be done automatically
  3. `./social_log/twitter.json`
     * `consumer_key` you can get from: [twitter Developers](https://developer.twitter.com)
     * `consumer_secret` you can get from: [twitter Developers](https://developer.twitter.com)
     * `access_token` you can get from: [twitter Developers](https://developer.twitter.com)
     * `access_token_secret` you can get from: [twitter Developers](https://developer.twitter.com)
  
</details>

# Credits

Please credit Gir0fa.
I spent a long time to gte this to work.
You don't even have to do that much just keep Gir0fa#6723 in its status somewhere.

Bot ORIGINALLY Coded by Tomato#6966 but maintaned by [Gir0fa#6723](https://dsc.gg/dscdev)
