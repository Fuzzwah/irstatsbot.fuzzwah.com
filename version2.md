---
title: iRacing Stats Discord Bot - Version 2
---

# Version 2 Overview

Over the last few weeks I've been working on a huge refactor of the [iRacing Stats Bot](http://irstatsbot.fuzzwah.com). This effort saw me make 89 pull requests, and had a combined count of 417 commits (my development process sees me pushing a commit every time I want to test a change).

This massive refactor included many changes which remove manual tasks from the operation of the bot. Generally these tasks were required during the season change over (which happens 4 times a year). In theory, the bot should now hum along with out intervention across the end of one season and the start of another.

# Highlight Improvements

* The collection of every race's results will now occur within 3 minutes of the race finishing. Down from a max of ~30mins.
* No issues caused if/when iRacing change the name of a series mid season.
* Solved problems caused by similarly named series being picked up as the same series.
* My custom "short names" for series no longer need to be a sub-string of the actual official name.
* Bot now deals with the new "the road tracks in oval series affect road ratings" change recently made by iRacing.
* The new database schema and refactored queries have seen massive improvements in performance.
* Dealing with divisions is now totally automated and works across all series (even the year long NASCAR and Indy series)
* Consistant formatting of titles of the output images.
* Huge improvements to the system used to have a command filter series, car class, season, week number, extra drivers to highlight, etc

Arugably even more important than the improvements listed above; I've solved a number of holes I'd dug myself into due to the organic way the bot had evolved up to the end of the "version 1" branch. I've cleared a path forward to work on many excellent much requested features that although they sounded simple were actually either extremely difficult to hack in or downright impossible due to choices made early on in the development of the bot.

# Git Stats

Here's the git stats showing the line count changes across the files that make up the bot:

```
 discord-bot/bot.py                     | 1846 +++++++++++++------------
 discord-bot/collection_checker.py      |    6 +-
 discord-bot/constants.py               |   45 +-
 discord-bot/divisions.py               |  247 ----
 discord-bot/drivers.py                 |  181 ++-
 discord-bot/seasons.py                 |  204 ++-
 discord-bot/seasons_info/__init__.py   | 1747 -----------------------
 discord-bot/stats.py                   | 2382 ++++++++++----------------------
 discord-bot/tester/run_tests.py        |   15 +-
 discord-bot/utils.py                   |  949 +++----------
```

Below are the squashed pull requests into the new version branch:

```
tidy up (5 minutes ago)
!week (9 minutes ago)
!dvr scott wood imsa (5 hours ago)
!dvr scott wood imsa (6 hours ago)
big titles (18 hours ago)
doc_strings (18 hours ago)
titles (18 hours ago)
titles (19 hours ago)
sof mc (20 hours ago)
driver season (22 hours ago)
champ (22 hours ago)
driver (22 hours ago)
add_driver (22 hours ago)
drivers (22 hours ago)
add_driver (22 hours ago)
remove some debug shit (22 hours ago)
maint option (22 hours ago)
make tmp/html dir (23 hours ago)
drivers (24 hours ago)
defaults (24 hours ago)
defaults (25 hours ago)
ir_seasons is dead (25 hours ago)
ir_seasons is dead (26 hours ago)
sched link (26 hours ago)
series (26 hours ago)
series (2 days ago)
clear defaults (2 days ago)
default series (2 days ago)
catid not category name (2 days ago)
drivers (2 days ago)
lastrace (2 days ago)
cleanup (2 days ago)
week (2 days ago)
default series (3 days ago)
week (3 days ago)
pts (3 days ago)
sched (3 days ago)
laps (3 days ago)
offs part sof (3 days ago)
champ (3 days ago)
lastrace (3 days ago)
remove spaces at end of lines (3 days ago)
reeeeeefuct0r (3 days ago)
reeeeeefuct0r (4 days ago)
split parse_command out into sep funcs (4 days ago)
seasons refactor (5 days ago)
(origin/new-schema) seasons refactor (7 days ago)
seasons refactor (7 days ago)
seasons refactor (8 days ago)
(new-schema) SEASONS refactor (8 days ago)
sched in db (8 days ago)
full sched (9 days ago)
auto driver name does not need sub flagged (12 days ago)
fs sched (12 days ago)
auto add subbed user to !driver if no name supplied (13 days ago)
USF 2000 Championship weekly (13 days ago)
remove some debug (13 days ago)
NEC (2 weeks ago)
!drivers (2 weeks ago)
!part (3 weeks ago)
!drivers (2 weeks ago)
single laptime func (3 weeks ago)
where 1 = 1 (3 weeks ago)
!dvr radecki grzegorz w4 road (3 weeks ago)
srf hock (3 weeks ago)
single laptime func (3 weeks ago)
!lastrace team (3 weeks ago)
timer for !driver (3 weeks ago)
time format boxplot (3 weeks ago)
week number (3 weeks ago)
MC (3 weeks ago)
!driver Rob Crouch (3 weeks ago)
road, oval, dirt_road, dirt_oval (3 weeks ago)
!lastrace oval Chris J Roberts (3 weeks ago)
no cmd names needed in decorators (3 weeks ago)
things (3 weeks ago)
command name dupe in errors (3 weeks ago)
!rlaps a-fix (3 weeks ago)
switch to using seasonid for all queries not series_name (4 weeks ago)
usfk2k (5 weeks ago)
points prolly broke champ (5 weeks ago)
laps (5 weeks ago)
qlaps (5 weeks ago)
utils and some work on stats (5 weeks ago)
stats work (5 weeks ago)
utils and some work on stats (5 weeks ago)
results table work (5 weeks ago)
lastrace (5 weeks ago)
initial util (5 weeks ago)
initial bot.py (5 weeks ago)
```