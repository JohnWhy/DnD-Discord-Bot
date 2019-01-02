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
