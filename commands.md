---
title: iRacing Stats Discord Bot - Commands
---

## Commands

In the examples below, square brackets have been used to show the required arguments for each command. Round brackets have been used to show optional arguments that can be provided to provide more fine grained responses.

For some commands you can specify a particular week or season. To select a week you include a **w#** argument, where the # is replaced by the week you want; for example **w1** for week 1 of the season. To select a season you include a **##s#** argument, where the first two numbers are the year and the final number is the season; for example **20s3** for 2020 Season 3. If a season or week isn't specified, the bot will return information about the current week and/or season.

For some commands where it makes sense, if you specify a multiclass series you will need to provide an argument to also specify which class you're interested in.

Many commands have a shorter alias that can be used.

### Standard Commands:
### `!series [category]`
> Displays a table of series and the abbreviations to use for each of them in all the other commands. The category must be provided; either **road**, **oval**, **dirt**, **rx**, or **offroad**.

### `!schedule [series abbrev]`
> Track schedule for a series. 
> Alias: `!sched`

### `!driver [driver name] (category) (w#) (##s#) (series abbrev)`
> Returns statistics about a driver's current season. If no category is provided the bot will return the output for the category that the driver has raced the most this season. You can also filter the information returned to a single series by providing a series abbreviation.
> Alias: `!dvr`

### `!lastrace (category) (series abbrev)`
> Returns information about a driver's most recent race.

### `!championship [series abbrev] (##s#)`
> Output a table displaying the top 30 drivers in the championship standings. 
> Alias: `!champ`

### `!strengthoffield [series abbrev] (w#) (##s#)`
> Outputs a heatmap showing the strength of field of each time slot. 
> Alias: `!sof`

### `!officialsessions [series abbrev] (w#) (##s#)`
> Outputs a heatmap showing the number of times each time slot had official sessions. 
> Alias: `!offs`

### `!participation [series abbrev] (w#) (##s#)`
> Outputs a heatmap showing the participation for the series. 
> Alias: `!part`

### `!qualifyinglaps [series abbrev] (w#) (##s#)`
> Returns a table and scatter plot displaying the week's best qualifying times. 
> Alias: `!qlaps`

### `!racelaps [series abbrev] (w#) (##s#)`
> Returns a table and scatter plot displaying the week's best race lap times. 
> Alias: `!rlaps`

### `!averageracelaps [series abbrev] (w#) (##s#)`
> Returns a table and scatter plot displaying the week's best average race lap times. 
> Alias: `!arlaps`

### Utils:
### `!litres2gallons [number]`
> Converts gallons to litres. 
> Alias: `!l2g`

### `!celsius2fahrenheit [number]`
> Converts celsius to fahrenheit. 
> Alias: `!c2f`

### `!gallons2litres [number]`
> Converts gallons to litres. 
> Alias: `!g2l`

### `!fahrenheit2celsius [number]`
> Converts fahrenheit to celsius. 
> Alias: `!f2c`

### `!kph2mph [number]`
> Converts kilometers per hour to miles per hour. 
> Alias: `!k2m`

### `!mph2kph [number]`
> Converts miles per hour to kilometers per hour. 
> Alias: `!m2k`

### Team Subscriber Admin Commands:
### `!default_series [series abbrev]`
> Sets the default series for a discord guild. With this set, if a command that requires a series abbrev is triggered with out a series being specified, it will fall back to the default.

### `!default_category [category]`
> Sets the default category for a discord guild.

### `!add_driver [driver name] [color hex] [@discord handle]`
> Adds a driver to a discord guild.

### `!remove_driver [driver name]`
> Removes a driver to a discord guild.

### `!update_driver [driver name] [color hex]`
> Updates a driver's highlight color.

### Subscription Required Commands:
### `!points [series abbrev] (##s#)`
> Returns three pieces of information; a table displaying the top 5 drivers in the series, along with highlighted team drivers. A table showing the points each driver has locked in for each week of the season, highlighting dropped weeks and the lowest current week's points (so you know what you need to beat to improve). Finally a line chart is included to give a good visual overview of each driver's championship season.
> Alias: `!pts`

### `!week [series abbrev] (w#) (##s#)`
> Returns information about how many races the team's drivers have completed this week in the series, along with the number of championship points they have currently for the week.

### `!drivers (category) (irchange)`
> Returns a list of the team's drivers, along with some basic information such as number of races for the season, current iRating and iRating gain/loss for the season. By default the driver's information will be for the category they've raced the most for the season, optionally you can specify a category type (road, oval, dirt, rx, offroad) to get the details for each driver in that category. If the `irchange` argument is provided the list of drivers will be sorted by iRating gained.

