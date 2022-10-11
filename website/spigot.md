![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/Main.png?raw=true)

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

# Introduction to Streamline

### What is Streamline?
`Streamline` or possibly known as `StreamlineCore` is a **Minecraft Java Edition** server plugin for both proxies *and* backend servers.

Things we call "`Modules`" allow your server to have vast capabilities through this `Core` plugin.

`Modules`, simply put, are plugins (like those for your **Minecraft Server**) but for `StreamlineCore`. Think of it like a house: the `StreamlineCore` is the foundation to the house and the `Modules` are things such as appliances or even rooms in the house.

### What makes Streamline special?
`Streamline` allows for **universal cross-platform capabilities** with its `Modules`.

This essentially means you can <u>run the same modules on a BungeeCord proxy that you would on a Velocity proxy</u> (or even a Spigot or Paper backend server). This, coupled with the `Modularized` features means that **you**, the server admin, can choose *exactly* what you want in your server.

This also makes it very simple for server to use a specific module **across your servers**, or even for `Developers` to **develop modules for your server** (or the community).

### What exactly is Streamline capable of?
Literally *anything*.

#### Supported Proxies:
> * Velocity
> * Bungeecord
> * Waterfall
> * Flamecord
> * Travertine

#### Supported Backend Servers:
> * Spigot.
> * Paper.
> * Purpur.
> * Tuinity.

#### Natively-Supported Plugins:
> * Luckperms.
> * Geyser.
> * PlaceholderAPI.

![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/JoinTheDiscord.png?raw=true)

**Please join the Streamline Discord in order to get updates and for me to fully assist you with bugs, questions, or suggestions.**

Streamline Discord: [**click here**](https://dsc.gg/streamline)

![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/Dependencies.png?raw=true)

MUST HAVE:
- LuckPerms latest. [**[ FOUND HERE ]**](https://luckperms.net/download)
- Java **16 or higher**. [**[ FOUND HERE ]**](https://jdk.java.net/archive/)
  - **NOTE: *If you are using PebbleHost, you will need to install Java 16 a little different. There is an article on how to do this*** [**[ FOUND HERE ]**](https://help.pebblehost.com/en/minecraft/does-pebblehost-support-java-11-16-17-18)***.***

![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/DiscordSetupHelp.png?raw=true)

Follow the Discord setup guide [**[ FOUND HERE ]**](https://github.com/Streamline-Essentials/StreamlineWiki/wiki/Discord-Setup) to set up the discord module.

# What can I do with the `Discord Module`?
- Link **Discord to Minecraft** and **Minecraft to Discord** with `Routes`.
  - Available link types:
    - <u>Natively</u> (Without other Modules):
      - **Proxy local chat** `<->` **Discord Text Channel**
      - **Proxy global chat** `<->` **Discord Text Channel**
      - **All online players with specific permission** `<->` **Discord Text Channel**
      - **Discord Text Channel** `<->` **Discord Text Channel**
    - <u>Groups</u> (With `StreamlineGroups` Module):
      - **Guild chat** `<->` **Discord Text Channel**
      - **Party chat** `<->` **Discord Text Channel**
    - <u>Messaging</u> (With `StreamlineMessaging` Module):
      - **Local Room chat** `<->` **Discord Text Channel**
      - **Global Room chat** `<->` **Discord Text Channel**
      - **Custom Room chat** `<->` **Discord Text Channel**
  - Message formats are completely customizable.
  - Avatar with player's skin will pop up when their message is sent to Discord.
- Link player's Discord profile with your server.
  - Players can chat using their StreamlineUser profile from Discord.
- All Discord messages can be configured to be sent as <u>completely customized Discord embedded messages</u>

![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/CommandsAndPermissions.png?raw=true)

### NOTICE ABOUT COMMANDS
***All commands are completely customizable in their `.yml` file.***

### NOTICE ABOUT PERMISSIONS
***All permissions are completely customizable in their command's `.yml` file.***

### Information about Command Syntax
| When we say...  | We mean...                                                                                                                                  | Notes                                                                              |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| `user`          | Any player that has every joined your server. They can even be offline.                                                                     |                                                                                    |
| `input`         | A collection of typed characters in a command.<br/>Example: in the words "Hello, there!", "there" is the 2nd `input`.                       | Also known as an `arg`, `argument`, `param`, or `parameter`.                       |
| `string`        | An input that is text.<br/>Example: "Hello. This is a string"                                                                               |                                                                                    |
| `syntax-key`    | Anything from this list table.                                                                                                              |                                                                                    |
| `syntax-input`  | Any input that was described by a `syntax-key`.                                                                                             |                                                                                    |
| `syntax-key...` | Any number of space-separated inputs.<br/>Example: for a "`string...`" syntax, you could supply the command "string1 string2 thing3 thing4" | "`<syntax-key>`" in the first column, is replaced by its definition in this table. |
| `<syntax-key>`  | That input is required if prior `syntax-input` was supplied and is of type "`<syntax-key>`"                                                 | "`<syntax-key>`" in the first column, is replaced by its definition in this table. |
| `(syntax-key)`  | That input is optional and is of type "`<syntax-key>`"                                                                                      | "`<syntax-key>`" in the first column, is replaced by its definition in this table. |
| `integer`       | An input that is a number that *does not* have a **decimal**.                                                                               |                                                                                    |
| `decimal`       | An input that is a number that *does* have a **decimal**.                                                                                   |                                                                                    |

### Commands Provided by `StreamlineCore`
| Command Syntax                                            | Description                                                                                                                                                                                                                                                                      | Permissions                                                                       |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `/parse <user> <string...>`                               | Parses the provided string of text on the user with Streamline's `RAT API` (Replace a Thing API); which is a PlaceholderAPI built into Streamline. Parses placeholders such as `%streamline_user_play_minutes%` or `%<placeholder-identifier>_<parameters for the placeholder>%` | `streamline.command.parse.default`**:** allows access to full command.            |
| `/streamline-reload`                                      | Reloads the entire plugin.                                                                                                                                                                                                                                                       | `streamline.command.streamlinereload.default`**:** allows access to full command. |
| `/pxp <user> <xp / level> (set / add / remove) <decimal>` | Sets, adds, removes, or checks a user's `Streamline` xp or level (leveling system).                                                                                                                                                                                              | `streamline.command.proxyexperience.default`**:** allows access to full command.  |
| `/pplaytime <user> (set / add / remove) <decimal>`        | Sets, adds, removes, or checks a user's `Streamline` playtime.                                                                                                                                                                                                                   | `streamline.command.proxyexperience.default`**:** allows access to full command.  |
| `/ppoints <user> (set / add / remove) <decimal>`          | Sets, adds, removes, or checks a user's `Streamline` points.                                                                                                                                                                                                                     | `streamline.command.points.default`**:** allows access to full command.           |
| `/ptag <user> (add / remove) <string...>`                 | Adds, removes, or checks a user's `Streamline` tags.                                                                                                                                                                                                                             | `streamline.command.tag.default`**:** allows access to full command.              |
| `/module <reload / reapply> (string...)`                  | Reloads or reapplies either all `Modules` or a specific set of `Modules`.                                                                                                                                                                                                        | `streamline.command.streamlinemodule.default`**:** allows access to full command. |


![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/HowToInstall.png?raw=true)

1. Download the plugin file.
2. Drop it into your server's plugins folder.
3. Start and stop your server.
4. Fill out the configs where necessary.
   - Configurations for the streamline plugin can be found in your `plugins` folder, under `StreamlineAPI` (or `streamlineapi` if using Velocity).
5. Add desired modules.
   - Modules can be downloaded from here: [click here](https://github.com/Streamline-Essentials/StreamlineWiki/wiki/Modules#download)
6. Start and stop your server again.
7. Fill out module configs where necessary.
   - Module files can be found in your `plugins` folder, under `StreamlineAPI` (or `streamlineapi` if using Velocity), under `module-resources`.
8. Start your server again.

More information can be found on our wiki: [**click here**](https://github.com/Streamline-Essentials/StreamlineWiki/wiki/Modules#installation)

![Discord](https://github.com/Streamline-Essentials/StreamlineWiki/blob/main/website/images/NeedHelpSubmitBugs.png?raw=true)

1. Look on the wiki: [**click here**](https://github.com/Streamline-Essentials/StreamlineWiki/wiki)
2. Get in touch on the Streamline Discord: [**click here**](https://discord.gg/tny494zXfn)
3. Submit a bug on the issue tracker (this is rarely checked): [**click here**](https://github.com/Streamline-Essentials/StreamlineAPI/issues)

#### NOTICE ABOUT BUG REPORTS
The review section is not built or programmed in a way where I can effectively give you support. Please do the steps above to submit a bug. I am more than willing to help you, please just reach out first! If you do submit a bug in the review section, please at the very least update your review or write a new one when it gets fixed! Thank you!