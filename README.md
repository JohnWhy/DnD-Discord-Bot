# DnD-Discord-Bot BETA RELEASE
## Current Status
* Missing !LevelUp
* Backgrounds not implemented yet
* Still not entirely user-friendly
* Some print statements are messy

## About
A Discord Bot for D&amp;D Character Creation, Maintaining, and Progression

Unlike my previous bot this will be closed-source.  This repo is made only for install & usage instructions as well as bug tracking and feature requests.

## Adding D&DBot

Follow this link: https://discordapp.com/oauth2/authorize?client_id=481910793697493011&scope=bot
You can try the bot out in this discord: 

## Usage
- !createcharacter [name] -- gets you started on the character creation
- !help -- tells you to come here
- !d20 -- rolls d20
- !d12 -- rolls d12
- !d10 -- rolls d10
- !d8 -- rolls d8
- !d6 -- rolls d6
- !d4 -- rolls d4
- !coinflip - flips a coin
- !stat [stat] -- use !stat to sell all of your sheet, !stat character, !stat spell, !stat skills, !stat equipment to see specific pages
- !set [attribute] [whatever] -- Case sensitive for now, used to change items on the character sheet

ex: !set XP 500

- !add [attribute] [whatever] -- Case sensitive as well

ex: !add CurrentHP 5

ex: !add Treasure Gold Chain

ex: !add Equipment Bone Club

- !rem [attribute] [whatever] -- Case sensitive

ex: !rem CurrentHP 2

ex: !rem Personality Bad Guy

ex: !rem Treasure Gold Chain

- !setk [dict] [key] [what to set it to] -- The clunkiness of this will be fixed later for easier management

ex: !setk Skills AnimalHandling 6

ex: !setk CharacterDescription Age 500

ex: !setk Modifiers Str 5

ex: !setk Stats Con 10

ex: !setk SavingThrowStats Wis 500000

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



## Donator Benefits NOT AVAILABLE YET

* More character slots
* Access to download a physical copy of your character sheet in standard D&D 5E format, filled with your most up-to-date stats.
* More to come...
