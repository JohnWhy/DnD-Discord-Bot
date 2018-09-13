# DnD-Discord-Bot BETA RELEASE
## Currently being worked on
* Missing !LevelUp
* Still not entirely user-friendly - being worked on
* A better bot usage guide with pictures

## About
A Discord Bot for D&amp;D Character Creation, Maintaining, and Progression

Unlike my previous bot this will be closed-source.  This repo is made only for install & usage instructions as well as bug tracking and feature requests.

## Adding D&DBot

Follow this link: https://discordapp.com/oauth2/authorize?client_id=481910793697493011&scope=bot&permissions=379968

You can try the bot / get support for it in this discord: https://discord.gg/XhtCeH9

## Usage
- !createcharacter [name] -- gets you started on the character creation
- !deletecharacter [name] -- deletes a character CANNOT BE UNDONE WITHOUT RECREATING !createcharacter
- !changechar [name] -- changes you to a different character, leave input blank if you want a list of your characters
- !help -- tells you to come here
- !d20 -- rolls d20
- !d12 -- rolls d12
- !d10 -- rolls d10
- !d8 -- rolls d8
- !d6 -- rolls d6
- !d4 -- rolls d4
- !coinflip - flips a coin
- !stats [stat] -- use !stat to sell all of your sheet, !stat ch[aracter], !stat sp[ell], !stat sk[ills], !stat eq[uipment] to see specific pages **NOTE:** b[lah] 'lah' is optional in command, meaning !stat ch shows the same as !stat character.

**BELOW COMMANDS ARE CASE SENSITIVE FOR CHARACTER SHEET MODIFYING** 

- !setk [dict] [item] [what to set it to] -- The clunkiness of this will be fixed later for easier management

- !kadd [dict] [item] [what you're adding to it] -- clunkiness will be fixed later

- !ksub [dict] [item] [what you're subtracting from it] -- clunkiness will be fixed later

**NOTE:** These are the ONLY 3 commands to modify Skills, CharacterDescription, Modifiers, Stats, Coins and SavingThrowStats currently.

ex: !setk Coins Electrum 500

ex: !kadd Coins Gold 5

ex: !setk Skills AnimalHandling 6

ex: !kadd Skills SleightOfHand 1

ex: !setk CharacterDescription Age 500

ex: !ksub CharacterDescription Age 1

ex: !setk Modifiers Str 5

ex: !ksub Modifiers Str 1

ex: !setk Stats Con 10

ex: !setk SavingThrowStats Wis 500000 -- This is the Saving Throws Modifiers mini-page.

- !set [attribute] [whatever] -- Case sensitive for now, used to change items on the character sheet

**NOTE:** This only works with items on CHARACTER SHEET and SPELLS & CANTRIPS which can be viewed using !stat ch or !stat sp

ex: !set XP 500

ex: !set Alignment Neutral Evil

- !add [attribute] [whatever] -- Case sensitive as well

ex: !add CurrentHP 5

ex: !add Treasure Gold Chain

ex: !add Equipment Bone Club

- !rem [attribute] [whatever] -- Case sensitive

ex: !rem CurrentHP 2

ex: !rem Personality Bad Guy

ex: !rem Treasure Gold Chain

- !appearance [Age] [Height] [Weight] [Eyes] [Skin] [Hair]

ex: !appearance 20 6'0 180 Blue Tan Brown

**FOR SERVER OWNERS**
Upon adding the discord bot to the server, make sure it has permissions to send messages.  That is about all it will need.

**FOR PLAYERS**
You can also message the bot in private, however it will have !d4, !d6 !d8 !d10 !d12 !d20 and !d100 commands as well as !coinflip to assist in playing the game itself.  These commands are probably best done in your public discord chat, but discuss with your DM how you want to handle it.

* To create a character, use !createcharacter [Name]

From there, the bot will guide you on what you need to do to get set up.  Again, this process best done in private, if multiple people are making characters in 1 chat, it might get confusing.

**If you're using a custom class / race**, you can enter "Custom" on those fields, but be aware that you'll be in charge of choosing your proficiencies and other relevant info to your character.  Meaning manually setting the attribute fields using the proper commands.  In other words, more work for you.

Your character will be available on ANY server that the bot is present on.  Your character progress is persistent and saved.  
Due to character informaton being stored on my own server, **You are limited to 3 characters per discord account**.  There will be an option to donate to unlocked more / unlimited characters.  Again, this is a space issue.  If more people donate, I can afford better hardware, which means bigger harddrives, which means I can afford to store all your character data.



## Donator Benefits TBD
* Unlimited character slots
* Access to download a pdf copy of your character sheet in standard D&D 5E format, filled with your most up-to-date stats.
* DM Tools (quick monster creation)
* Level up

**NOTE:** I'm currently swamped at work, so these benefits are going to take time to finish, currently more character slots is the only one you can get, but I'm not offering it until I feel the quality of the bot warrants people donating.
