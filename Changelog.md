# v1.3.4
- Fixed a bug where !search would spam chat if no index was given.

# 1.3
## NEW COMMANDS:
- `!givechar @user character`
    - ex: !givechar @Stoner Ronin --- This will give the discord user Stoner my character sheet for Ronin
- `!search category item`
    - ex: !search spells random
    - ex: !search help --- will give a detailed list of categories you can search
    - Major shoutout to the people maintaining https://www.dnd5eapi.co/api/ which allowed me to get this command completed
- `!get_random_monster rating_min rating_max`  --- Alternatively !grm works as a shortcut
    - ex: !grm 0 0.25 --- Will give a random monster with a challenge rating between 0 and 0.25
    - Again, major shoutout to https://www.dnd5eapi.co/api/ which allowed this command to be completed
- `!whatsmyprefix` --- HARDCODED to work with `!`, will give users the server prefix
    - Reminder that `!prefixreset` is also hardcoded and only users with `guild_permissions.administrator` can use this.
    - If a user uses this command they will be told the current server prefix now.

## NEW RACES:
- Added numerous new races per user suggestions

## Server Side Changes:
- File structure changed so that everyone has individual shelves containing their background, classes, and races:
- - This will allow custom backgrounds, classes, and races to be stored for individuals
- - Also planned for discord guilds to be allowed to store their own custom backgrounds, classes, & races.

## Bugfixes:
- Fixed bug that allowed anyone to `!changeprefix` and `!prefixreset` (Surprised this wasn't reported)

# 1.2.8.7
- fixed bug with subtracting in !r
- !help now displays different msg

# 1.2.8.6
- added Deception to Warlock during Character Creation Process (thanks Thijmen#5768 for finding this error)
- added alias for `!appear` to work as `!appearance`

# 1.2.8.4/5
- misc bug fixes
- fixed typos in certain classes
- fixed character creation process not working over PMs/DMs

# 1.2.8.3
- fixed bug where multi-word !set cmds weren't properly being set.

# 1.2.8.2
bug fixes:
- fixed bug where !createstats wasn't working for users who tried to make a character in between sql db transfer and now.
    - If you experience the above bug, use !activechar and select the character you attempted to make, then !createstats
- added disclaimer that + and - prefixes break the roll command
- fixed issues where errors in commands weren't properly explaining what went wrong.
- fixed stat generation on high elfs (they were getting an extra +1 to charisma that they shouldn't have)
- fixed saving throw modifier generation (was adding an additional modifer that it shouldn't have been)
- fixed numerous bugs related to character names, creating characters, deleting characters, changing names etc.

# 1.2.8.1 
bug fixes:
- bot becoming unresponsive occassionally has been fixed (stats, createcharacter, etc)

optimizations:
- bot is now storing data in SQL DB, which will respond quicker than the previous method, and not be affected by multiple shards accessing at the same time.
- checking for number of characters has been changed (this wont affect users)
- laid some groundwork for v1.3 5E DB

# 1.2.8
bug fixes:
- changed storage of prefixes to a more permanent solution that won't break anymore.
- fixed bug causing bot to be come unresponsive

optimizations:
- now on_command instead of on_message
- better scalibility for future updates

changes:
- prefixes have been reset as a result of the switch to the new format, this should be the last time they're wiped.

# 1.2.7.4
bug fixes:
- fixed bug where silver, electrum, and copper couldn't be added or set (thanks ElijahD#5073 for the report)

# 1.2.7.3
more optimizations

bug fixes:
- fixed bug that caused bot to be impossible to start related to !changeprefix being abused:
    - acceptable prefixes are here: 
    ```!@#$%^&*~)(-=_+][;':,.?```
    - you can use any combination of these, so `#$` is a valid prefix, as is just `?`
    
# 1.2.7.2
optimizations
- added a bot controller to launch bot with optimal settings and manage sharding
    - controller does what AutoShardedClient wishes it did optimally, AutoShardedClient didn't play nice enough with discord API during peak times, so this new solution means increased uptime, better response time, and more control for me over how many shards are open / need to be open.


# v1.2.5/6
bug fixes:
- fixed bug with subtraction not working in !r command.
- removed custom classes until a proper implementation is done
   - if you want to do a custom class, select one similar to the class you want to build, then modify the name in the character sheet after stat generation is complete.  Currently Custom classes aren't generating any stats properly.
- other stuff i can't remember now

# v1.2.4
optimizations:
- added additional error handling
- optimized !stats command to display much quicker.

# v1.2.3
bug fixes:
- fixed bug that caused featurerequests & bug reports to be sent to the void

# v1.2.2
optimizations:
+ bot responses to improper commands / command suggestions will now show that server's specific prefix instead of the default "!" prefix.

changes:
+ added "Loading..." presence when bot is restarting (can't test since it loads too fast)
+ additional information added to !info (including guides)
+ added Cantrips/Spells to pdf generation
+ pdfgen is now a donator-only command


# v1.2.1.1
## changes:
+ added roll guide to !r - https://github.com/Sp4zzy/DnD-Discord-Bot/blob/master/Rolling%20Guide.md
+ modified r[oll] command behavior, now the + modifier is added after all rolls are completed, instead of added to each roll.
     * ex: !r2d6 + 10 with 2 rolls of 3 and 4, will become sum 17, instead of 13+14=27
+ r[oll] command now accepts kh & kl per request here: https://github.com/Sp4zzy/DnD-Discord-Bot/issues/3
     * ex: !r2d20kh1 will roll 2 d20, and report the highest roll.
     * ex: !r5d20 kl 2 will roll 5 d20s and report the lowest 2.
+ r[oll] command now also accepts +/- of stats / skills.
     * ex: !r1d20+AnimalHandling will roll a d20 and add your AnimalHandling
     * ex: !r1d 20 + Str will roll a d20 and add strength modifier
+ raised r[oll] limit from 10 to 25.
## bug fixes:
+ fixed issue on character creation where old kadd command was told to be used.
+ fixed issues on character creation that allowed improper number of prof to be chose
+ fixed issue with placement of adding bonus lang/prof/mods/feats


# v1.2.0
## new commands:
- listchar[arcters] - gives a list of all characters
- pdfgen - gives a downloadable pdf, currently in it's early stages, 
NOTE: Make sure to open the pdf in Chrome/Mozilla/Edge, else strangeness can occur.   This feature will be available to all for a limited time, then will become a donator-only feature.
- checkdonator - gives True or False, True if user is a donator, False if they are not, no parameters

## optimizations:
- add, set, del now all have proper checking and feedback when command is given.

## changes:
- info - command gives a bit more info / formatting changes
- removed [' and '] from lists when presented to user
- set, add, and del now also double as kset, kadd, and kdel (kset, kadd, and kdel have been removed)
- CharacterDescription, Coins, Skills, Modifiers, Stats, SavingThrowStats is no longer required as a key when using set, add or del

previous: !kset Coins Platinum 500
current: !set Platinum 500

previous: !kadd Modifiers Str 5
current: !add strmod 5

previous: !kdel SavingThrowStats Dex 2
current: !del DexSt 2

previous: !kset Stats Str 5
current: !set Str 5

Reminder: these are all case-insensitive, meaning you can type DeXsT or Dexst or dexst, it's all the same to the bot.

## bug fixes:
- fixed typo in Vizier which made Religioon a proficiency
- bug that made it so the bot couldn't be PM'd

# v1.1.2
## NOTE:
- command prefixes have been wiped due to a bug during a backup, you'll need to reset your prefix with !changeprefix
- this update may have some oddities, bugs, or performance issues.  If you experience any, please report them in the issues section, or with !bugreport

## optimizations:
- roll command will now print multiple rolls all at once, and give a sum of all those rolls, instead of printing one at a time.
- transitioning from discord.py 0.16.14 to 1.0.0a

## new commands:
- info - gives information about the bot.




# v1.1.1

## new command:
- !prefixreset - admin only, resets prefix to default "!" (hardcoded so that prefix changes won't effect it, it will always be exactly "!prefixreset")

## optimizations:
- fixed a bug where Created Users wouldn't update automatically

# v1.1

## new commands:
- changeprefix - admin only
- del - replacement for rem
- erasecharacter - replacement for deletecharacter
- delk - replacement for remk
- addk - replacement for kadd
- changelog - gives changelog

## optimizations:
- stats now only tries to load what's needed, and displays output as it's loading.
- changechar has been fixed (but in different way from current deployment)

## changes:
- commands to modify no longer case sensitive (i.e. !setk Coins Electrum 500, will work as !setk cOins eleCtruM 500)
- shelve files are renamed on character rename, meaning !changechar will use your new name
- botstatus now auto-updates with version & total user accounts created

## current issues:
- none known
