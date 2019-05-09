
# Tom_The_Geek's Spigot Plugins

This is the official for my SpigotMC plugins

## A Quick Note

The plugins will be split into seperate pages at some point but for now I can only list them in one page. All documentation for each will also be available through its wiki on the GitHub repo

## ChatMinistrator
### Features

 - Fully automatic chat moderation split into two customisable operations: Caps detection and a customisable blacklist
 - Caps detection: automatically block chat messages with more than one capital letter for every lowercase letter. This ratio can be changed in the config
 - Blacklist: Chat messages containing words in the blacklist will automatically be blocked and the player notified
 - Operator notification: Whenever a message triggers the filters, any online users with a certain permission will be notified. This message contains the players name and the type of event (CAPS, blacklist).

### Commands
#### /cmblacklistadd \<word\>
This command adds a word to the blacklist.
##### Aliases
/cmbadd \<word\>
/cmba \<word\>
#### /cmblacklistremove \<word\>
Removes the specified word from the blacklist
##### Aliases
/cmbremove \<word\>
/cmbrm \<word\>
#### /cmreload
Reloads the config file. Required to be run after modifying the config manually or after using /cmba or /cmbrm
##### Aliases
/cmrl
### Config file
#### Default Config
<code>checkCaps: true
capsScoreMax: 1
blacklistEnable: false
blacklist: []
alertOpsToCaps: true
alertOpsToBlacklist: true</code>
#### Default Config Breakdown
##### checkCaps: true
If true the plugin will block all messages with a higher score than the <code>capsScoreMax</code> setting.
##### capsScoreMax: 1
If the chat message has a score greater than or equal to this value and the setting <code>checkCaps</code> is true, the chat message will be blocked
##### blackListEnable: false
If this option is set to true, any chat message containing any word on the blacklist will be automatically be blocked
##### blacklist: []
This config option is quite self-explanatory. It allows you to configure the blacklist of banned words. Only takes effect if the setting <code>blackListEnable</code> is true
##### alertOpsToCaps: true
If true any online users with the permission node <code>chatministrator.notify</code> will receive a message telling them the event has occurred.
##### alertOpsToBlacklist: true
Does the same as the previous option but for blacklist events instead
### Permissions

| Permission node        | Command            | Description                                                                                                          |
|------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------|
| chatministrator.notify | N/A                | All online users with this permission will recive a notification of blacklist or caps events if setup in the config. |
| chatministrator.       | /cmblacklistadd    | Allows the player to add words to the blacklist                                                                      |
| chatministrator.       | /cmblacklistremove | Allows the player to remove words from the blacklist.                                                                |
| chatministrator.reload | /cmreload          | Allows the player to reload from the config.                                                                         |

## WIP Plugins
I am currently working on a few plugins 
