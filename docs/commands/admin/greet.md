# Greet Configuration Commands

!!! info
    
    These commands can be executed by Admins and Bot Manager only.

!!! info

    Use `bb vars` to see all available variables you can use in message or add-on message.
    Below is a picture reference for sections used in setting up greet messages. [Reference to section](https://cdn.discordapp.com/attachments/782443597122502707/993897637042466897/unknown.png).

Greet messages are enabled by default. You can modify message settings by using the `bb greet` command. The following commands are used to setup, edit, and remove greet configurations for your Discord server.

## Greet Channel Command

**Usage:** `bb greet channel <channel | disable>`

This command sets the channel where the bot will send random greet messages from a list of custom messages.

**Examples**

| Command                                      | Explanation                                 |
| -------------------------------------------- | ------------------------------------------- |
| `bb greet channel #welcome`                  | Sets the greet channel to #welcome           |
| `bb greet channel disable`                   | Disables the greet channel feature           |


## Greet Message Command

**Usage:** `bb greet message <message | disable>`

This command adds a message to the list of greet messages. The bot will send a random message from this list when a user boosts the server. You can add upto 3 messages without a premium plan but you can't edit or remove a single message. 

!!! info
    
    If you want to clear messages, you can use `bb greet message disable`.

**Examples**

| Command                                      | Explanation                                 |
| -------------------------------------------- | ------------------------------------------- |
| `bb greet message Thank you for boosting!`   | Adds "Thank you for boosting!" to greet messages |
| `bb greet message disable`                   | Clears all greet messages and disables greet message feature |


## Add-on Message Command

**Usage:** `bb greet addon <message | disable>`

The bot can send additional information along with the greet message in the form of an 'add-on' message.

!!! info
    
    This feature requires that embeds are enabled. By default, embeds are enabled, but if they were previously disabled, you can re-enable them using the command `bb greet embed enable`.

**Examples**

| Command                                      | Explanation                                 |
| -------------------------------------------- | ------------------------------------------- |
| `bb greet addon Welcome {username}!`         | Sets the addon message to "Welcome {username}!"  |
| `bb greet addon disable`                     | Disables the addon message feature          |

## Greet Image Command

**Usage:** `bb greet image <image_url | disable>`

This command adds an image URL to the list of greet images that the bot can send. The bot will randomly choose an image from the list to be sent along with the greet message. Non-premium users can add up to 2 images. To clear all greet images, use the `disable` argument. Note that you cannot edit or remove individual images without clearing the entire list and re-adding them.

**Examples**

| Command                                    | Explanation                                                                               |
| ------------------------------------------ | ----------------------------------------------------------------------------------------- |
| `bb greet image https://i.imgur.com/abc.jpg` | Adds the image at the URL `https://i.imgur.com/abc.jpg` to the list of greet images            |
| `bb greet image disable`                   | Clears the list of greet images and disables the image feature                              |


## Greet Emoji Command

**Usage:** `bb greet emoji <emoji | disable>`

This command sets an emoji that the bot will use for an automatic reaction on the default boost message. To disable the emoji, use the `disable` argument.

**Examples**

| Command                           | Explanation                                                                                           |
| --------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `bb greet emoji 🎉`               | Sets the bot to react with the "🎉" emoji on the default boost message                                 |
| `bb greet emoji disable`          | Disables the automatic reaction feature and the bot will not react with any emoji on the boost message |

## Greet React Command

**Usage:** `bb greet react <msg>`

This command sets which message the bot will use the emoji reaction on. The options are:

- `default`: the default system message (default)
- `custom`: the bot's custom greet message (if enabled)
- `both`: both messages

**Examples**

| Command                      | Explanation                                                                                                   |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `bb greet react default`     | The bot will react with the set emoji on the default system message when a booster joins the server.            |
| `bb greet react custom`      | The bot will react with the set emoji on the bot's custom greet message if enabled and when a booster joins the server. |
| `bb greet react both`        | The bot will react with the set emoji on both the default system message and the bot's custom greet message when a booster joins the server.
| `bb greet react disable`     | The bot will disable reaction feature on any message.


## Greet DM Command

`bb greet dm <enable | disable>`

:   This command enables or disables the bot sending the greet message in the Direct Message (DM) of the server booster.

**Usage:** : `bb greet dm <enable | disable>`

**Examples**

| Command                              | Explanation                                                                                                                |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `bb greet dm enable`                 | Enables the bot to send greet messages in the DM of the server booster.                                                      |
| `bb greet dm disable`                | Disables the bot from sending greet messages in the DM of the server booster.                                               |

## Booster Stats

`bb greet stats <enable | disable>`

:   This command enables or disables the bot sending booster stats, such as the total number of boosts and the server boost level, in the greet message. This is enabled by default.

## Test

`bb greet test`

:   This command sends a test greet message as configured.

## Embed

`bb greet embed <enable | disable>`

:   This command enables or disables the bot sending the greet message in an embed. This is enabled by default.

## Usage

:   `bb greet < channel | message | addon | author | author-icon | title | footer | footer-icon | image | dm | emoji | react | embed | thumbnail | stats | test >`
