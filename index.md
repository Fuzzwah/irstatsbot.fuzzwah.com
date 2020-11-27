## Overview

I have created a Discord bot that interacts with my iRacing Statistics database. The bot allows users to access a range of statistical information about iRacing Series and Drivers.

You can use this [Discord invite link](https://discord.gg/AFW8BDm) to join the iRacing Stats Discord where the bot will respond to commands in the #bot-playground channel. Feel free to check out your own stats for the current season using the `!driver Your Name` command. Below is an example of the type of information that the bot will respond with:

![!driver](https://user-images.githubusercontent.com/658935/100395468-255c5300-3095-11eb-8d52-dbfa5f1a7d5c.png)

Typing `!help` in the channel will have the bot private message you with a breif explanation of all the available commands.

You can [check out screenshots](screenshots.html) of the output from some of the other commands.

## Adding the bot to your Discord

The bot also has a range of features that support iRacing teams and communities. It is possible to add the bot to your own Discord server and configure a list of drivers to automatically include in the output of the various commands.

I have set up a Patreon page to allow people to subscribe to help cover the costs involved with running the bot.

[patreon.com/RobCrouch](https://patreon.com/RobCrouch)

If you're interested in adding the bot to your team's Discord please visit my Patreon page and select the [iRacing Stats Discord Bot: Team Access](https://www.patreon.com/join/RobCrouch/checkout?rid=5846445) member level.

## Individual subscribers

There are also a number of subcriber only commands that can any public Discord server, such as the iRacing Stats Discord, iRacing Open Wheel Hub, iRacing Chat, GermanSimRacing.de, and CTC Lotus 79.

The bot will highlight the subscribed driver in various outputs, as shown in the [screenshots](screenshots.html)]. If you're interested in supporting the project and getting access to the subscriber only commands, please visit my Patreon page and select the [iRacing Stats Discord Bot: Driver Access](https://www.patreon.com/join/RobCrouch/checkout?rid=5846474) member level.

## Commands

In the examples below, square brackets have been used to show the required arguments for each command. Round brackets have been used to show optional arguments that can be provided to provide more fine grained responses.

For some commands you can specify a particular week or season. To select a week you include a **w\#** argument, where the # is replaced by the week you want; for example **w1** for week 1 of the season. To select a season you include a **\#\#s\#** argument, where the first two numbers are the year and the final number is the season; for example **20s3** for 2020 Season 3. If a season or week isn't specified, the bot will return information about the current week and/or season.

For some commands where it makes sense, multiclass series you will need to provide an argument to specify which class you're interested in.

Many commands have a shorter alias that can be used.

### Standard Commands:
### `!series [category]`
Displays a table of series and the abbreviations to use for each of them in all the other commands. The category must be provided; either **road**, **oval**, **dirt**, **rx**, or **offroad**.
### `!schedule [series abbrev]`
Track schedule for a series. 

Alias: `!sched`
### `!driver [driver name] (category) (w\#) (\#\#s\#)`
Returns statistics about a driver's current season. If no category is provided the bot will return the output for the category that the driver has raced the most this season.

Alias: `!dvr`
### `!season [series abbrev] [driver name] (\#\#s\#)`
Returns information about a driver for a single series.
### `!lastrace (category) (series abbrev)`
Returns information about a driver's most recent race.
### `!championship [series abbrev] (\#\#s\#)`
Top 30 championship standings. 

Alias: `!champ`
### `!strengthoffield [series abbrev] (w\#) (\#\#s\#)`
Strength of field heatmap for the series. 

Alias: `!sof`
### `!officialsessions [series abbrev] (w\#) (\#\#s\#)`
Official session count heatmap for the series. 

Alias: `!offs`
### `!participation [series abbrev] (w\#) (\#\#s\#)`
Participation heatmap for the series. 

Alias: `!part`
### `!qualifyinglaps [series abbrev] (w\#) (\#\#s\#)`
Best qualifying times. 

Alias: `!qlaps`
### `!racelaps [series abbrev] (w\#) (\#\#s\#)`
The week's best race lap times. 

Alias: `!rlaps`
### `!averageracelaps [series abbrev] (w\#) (\#\#s\#)`
The week's best average race lap times. 

Alias: `!arlaps`

### Utils:
### `!litres2gallons [number]`
Converts gallons to litres. 

Alias: `!l2g`
### `!celsius2fahrenheit [number]`
Converts celsius to fahrenheit. 

Alias: `!c2f`
### `!gallons2litres [number]`
Converts gallons to litres. 

Alias: `!g2l`
### `!fahrenheit2celsius [number]`
Converts fahrenheit to celsius. 

Alias: `!f2c`
### `!kph2mph [number]`
Converts kilometers per hour to miles per hour. 

Alias: `!k2m`
### `!mph2kph [number]`
Converts miles per hour to kilometers per hour. 

Alias: `!m2k`

### Team Subscriber Admin Commands:
### `!default_series [series abbrev]`
Sets the default series for a discord guild.
### `!default_category [category]`
Sets the default category for a discord guild.
### `!add_driver [driver name] [color hex] [@discord handle]`
Adds a driver to a discord guild.
### `!remove_driver [driver name]`
Removes a driver to a discord guild.
### `!update_driver [driver name] [color hex] [@discord handle]`
Updates a driver's highlight color.

### Subscription Required Commands:
### `!points [series abbrev] (\#\#s\#)`
Championship points of the team's drivers. 

Alias: `!pts`
### `!week [series abbrev] (w\#) (\#\#s\#)`
Current week's points of the team's drivers.
### `!drivers`
Returns information about the team's drivers.



