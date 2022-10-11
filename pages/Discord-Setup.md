### Table of Content:
> * [**Key Information**](#key-information)
> * [**Installation**](#installation)
> * [**Bot Setup**](#bot-setup)
> * [**Plugin Setup**](#plugin-setup)
> * [**Route Setup**](#setting-and-removing-channel-routes)

# Key Information
Below is some much-needed information on things such as file locations and some `Streamline` terminology.

| When we say...                                                                                  | We mean...                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| your plugins folder                                                                             | The `plugins` folder in your server's main folder.                                                                                                         |
| streamline main folder                                                                          | The `StreamlineAPI` folder in your plugin's folder.<br/>***NOTE:** if you use Velocity, the folder will actually be called* `streamlineapi` *(lowercase)!* |
| modules folder                                                                                  | The `modules` folder in your streamline main folder.                                                                                                       |
| module resources folder                                                                         | The `module-resources` folder in your streamline main folder.                                                                                              |
| `<specified>` module folder<br/>***NOTE:** `<specified>` will be replaced with a module's name* | The `<specified>` folder in your module resources folder                                                                                                   |
| commands folder                                                                                 | The `commands` folder in your streamline main folder                                                                                                       |
| module commands folder                                                                          | The `commands` folder in your `<specified>` module folder.<br/>***NOTE:** `<specified>` will be replaced with a module's name*                             |


# Introduction
Ever wanted to **link Discord to your Minecraft server** or **your Minecraft server to Discord**? *Look no further!*

With the `StreamlineCore` **Java Minecraft** server plugin ([**found here**](https://www.spigotmc.org/resources/streamline-unlock-your-proxys-core-velocity-bungeecord-spigot-geyser-mc-1-7.83659/)) and one of its `Modules` ([**found here**](https://www.spigotmc.org/resources/105540/)) called `StreamlineDiscord`, *you can do just that*!

# Developer Mode
> Go to the `Advanced` tab and enable `Developer Mode` so you can use the `Copy ID` feature!

![Developer Mode](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/developer-mode.png?raw=true)

# Installation
1. Stop your server if it is running.
2. Put the `StreamlineDiscord` `Module` into your modules folder on your server.
3. Restart your server to assure the module loaded properly.
4. Stop your server again.
5. Edit the configurations for the `StreamlineDiscord` `Module` to your liking (if you need help, *see below*).
6. Start your server again.

# Bot Setup
1. Create a new application by clicking **New Application** at [**this link**](https://discord.com/developers/applications/).

![Create Application](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/new-application.png?raw=true)

2. Choose a name for your bot and click **Create**.

![Create Bot](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/name-it.png?raw=true)

3. Under the **Settings** tab, click **Bot**. Then click **Add Bot** and confirm with **Yes, do it**!
   - Keep `PUBLIC BOT` unchecked so only you can invite the bot to your server.

![Privileged Gateway Intents](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/add-bot.png?raw=true)
![Privileged Gateway Intents](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/yes-do-it.png?raw=true)

4. Under `Privileged Gateway Intents` in the **Bot** tab, turn on all three settings.
 
![Privileged Gateway Intents](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/privileges.png?raw=true)

5. Copy the `Application ID` from the application's `General Information` page.

![Copy Application Id](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/application-id.png?raw=true)

6. Paste the `Application ID` after `client_id=` in the link "`https://discord.com/oauth2/authorize?scope=bot&permissions=8&client_id=`" in your internet browser.
   - It should now look something like this: `https://discord.com/oauth2/authorize?scope=bot&permissions=8&client_id=871103022010277844`.
7. Complete the invitation and allow your bot to join your server.
8. You have set up the bot!

# Plugin Setup
1. Open the configuration file which can be found in your module resources folder under the `streamline-discord` folder.
2. Copy the `Token` of the bot from the application page.
3. Paste the token into the `config.yml` and set bot prefix and activity settings. The activity is what the bot is currently doing (will be displayed when the bot is online), it will look like "Playing... **something**" or "Streaming... **something**".
4. You have set up the plugin!

#### Default Configuration
```yml
# Discord bot settings.
bot:
  # The token of your discord bot.
  token: "<put token here -- DO NOT GIVE THIS TO ANYONE>"
  # The prefix for commands for your discord bot.
  prefix: ">>"
  # Settings for the activity or status of your bot.
  # With default settings, it will say ">>help for help!"
  # under your bot on the sidebar in your Discord server.
  activity:
    # Type can be:
    # CUSTOM
    # COMPETING
    # LISTENING
    # PLAYING
    # STREAMING
    # WATCHING
    type: CUSTOM
    # The value after said setting.
    # If above is "LISTENING" and this is "your suggestions",
    # it will say "Listening to... your suggestions"
    # under your bot.
    value: "**>>help** for help!"
```

# Setting and Removing Channel Routes
A `Route` is a connection between two types of `EndPoint`s, but for simplicity's sake, just think of it like a tunnel between two different rooms; where the "rooms" are `EndPoint`s, but the tunnel only goes one direction.

### Setting.
In Discord, in the channel you want to link with Minecraft, type the command: `<prefix><channel-command-alias> set <type> <identifier>`
> * `<prefix>` is the prefix in your `config.yml` file for the Discord module. By default, it is `>>`.
> * `<channel-command-alias>` is an alias of the discord-command with the identifier of `channel`. By default, you can use `ch`.
> * `<type>` is one of the types outlined below.
> * `<identifier>` is an identifier as described below depending on the `<type>`.

### Removing.
In Discord, in the channel you want to unlink from Minecraft, type the command: `<prefix><channel-command-alias> remove <type> <identifier>`
> * `<prefix>` is the prefix in your `config.yml` file for the Discord module. By default, it is `>>`.
> * `<channel-command-alias>` is an alias of the discord-command with the identifier of `channel`. By default, you can use `ch`.
> * `<type>` is one of the types outlined below.
> * `<identifier>` is an identifier as described below depending on the `<type>`.
>   * This is optional. If left empty, it will remove all `channels` with the type provided.

### `EndPoint` Types.
<b>Native with Streamline Discord Module</b>

`GLOBAL_NATIVE`
* Identifier: none.
* Global message.

`SPECIFIC_NATIVE`
* Identifier: server name.
* Localized message to one server.

`PERMISSION`
* Identifier: permission.
* Message to everyone on the Minecraft server with a specific permission.

`DISCORD_TEXT`
* Identifier: channel id (as stringed long).
* Message to be sent a specific discord text channel identified by the channel id.

<b>With Streamline Guild Module</b>

`GUILD`
* Identifier: guild uuid.
* Message to everyone in specified guild.

`PARTY`
* Identifier: party uuid.
* Message to everyone in specified party.

<b>With Streamline Messaging Module</b>

`SPECIFIC_HANDLED`
* Identifier: chat channel identifier.
* Message to everyone in specified chat channel.