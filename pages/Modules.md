### Table of Contents:
> * [**Key Information**](#key-information)
> * [**Introduction**](#introduction)
> * [**Download**](#download)
> * [**Installation**](#installation)

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
To put it simply: modules are the yeast to your bread; without them, the Streamline plugin would be nothing more than a shell. Modules are a way to add features to your server (proxies and backend alike) that are fitting for only your server.

The core plugin is an adapter for your modules to hook into the server. This means that a proxy-specific module will work on all supported proxies <i>without</i> a change of code. This makes it super simple for server owners and administrators to use a specific module across their servers, or even for developers to develop modules for your server (or the community).

### Supported Proxies:
> * Velocity
> * Bungeecord
> * Waterfall
> * Flamecord
> * Travertine

### Supported Backend Servers
> * Spigot.
> * Paper.
> * Purpur.
> * Tuinity.

### Natively-Supported Plugins.
> * Luckperms.
> * Geyser.
> * PlaceholderAPI.

# Download
These are the current download links to all modules.

### Streamline Utilities Module
> This is a module focused on providing helpful features in maintaining a Minecraft server -- especially one using Streamline.
> 
> Author: Quaintified

Link to download: [**click here**](https://www.spigotmc.org/resources/105543/)

### Streamline Messaging Module
> This is a module focused on providing messaging features.
>
> Author: Quaintified
>
> Currently offers:
> * Cross-network messaging.
> * Customizable chat rooms such as, but not limited to: staff chat, builders chat, global, local, or custom.
> * Ability to add, remove, or block friends. Very similarly to Hypixel.

Link to download: [**click here**](https://www.spigotmc.org/resources/105542/)

### Streamline Groups Module
> This is a module focused on providing features regarding groups such as guilds or parties.
>
> Author: Quaintified
>
> Currently offers:
> * Cross-network parties and guilds.
    >     * Invite, promote, demote, disband, chat.
>     * Completely customize groups' roles and their permissions.
>     * Guild specific:
        >         * Rename, customize guild leveling.

Link to download: [**click here**](https://www.spigotmc.org/resources/105541/)

### Streamline Discord Module
> This is a module focused on providing Discord integration for your server.
>
> Author: Quaintified
>
> Soft-depends (can hook into, but not required):
> * Streamline Messaging Module.
> * Streamline Discord Module.
    > Currently offers:
> * Cross-network parties and guilds.
    >     * Invite, promote, demote, disband, chat.
>     * Completely customize groups' roles and their permissions.
>     * Guild specific:
        >         * Rename, customize guild leveling.

Link to download: [**click here**](https://www.spigotmc.org/resources/105540/)

# Installation
### Recommended Installation (Stops the Server)
1. Download the module.
2. Stop your server.
3. Put the module (`.jar` file) into your modules folder.
4. Start your server.
5. Stop your server again.
6. Configure the module by looking in the module resources folder and finding the folder with the module's name.
7. Start your server again.

### Soft Installation (Does NOT Stop the Server)
1. Download the module.
2. Put the module (`.jar` file) into your modules folder.
3. Run the command `module reapply` from your server's console.
4. Configure the module by looking in the module resources folder and finding the folder with the module's name.
5. Run the command `module reapply` from your server's console again.