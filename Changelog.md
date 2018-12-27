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
