# 1.2.8.2
bug fixes:
- fixed bug where !createstats wasn't working for users who tried to make a character in between sql db transfer and now.
    - If you experience the above bug, use !activechar and select the character you attempted to make, then !createstats

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
