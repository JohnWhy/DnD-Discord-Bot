# v1.2.1.0
## changes:
+ modified r[oll] command behavior, now the + modifier is added after all rolls are completed, instead of added to each roll.

     * ex: !r2d6 + 10 with 2 rolls of 3 and 4, will become sum 17, instead of 13+14=27
+ r[oll] command now accepts kh & kl per request here: https://github.com/Sp4zzy/DnD-Discord-Bot/issues/3

     * ex: !r2d20kh1 will roll 2 d20, and report the highest roll.
     
     * ex: !r5d20 kl 2 will roll 5 d20s and report the lowest 2.
     
+ r[oll] command now also accepts +/- of stats / skills.

     * ex: !r1d20+AnimalHandling will roll a d20 and add your AnimalHandling
     
     * ex: !r1d 20 + Str will roll a d20 and add strength modifier

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
