# How to create custom races
## KEY

**string value** - Can be anything you want, but generally alphanumeric.
-- ex: race_name:Zyborg
**integer value** - Is 0-9 values (do not put alphanumeric in here or the command will fail)
-- ex: race_size:30
-- ex:number_of_bonus_languages:1
**list value** - Can be anything you want, but this field accepts multiple inputs in a list, so **separate each item/thing with a semicolon (;) character.**
-- ex: saving_throws:Str;Con
-- ex: equipment:Short Bow;Short Sword;Amulet of Magic 

## COMMAND /customracecreation
- race_name  --  (string value) *This is the name of the custom race, and will appear in the race selection list* 
- strength_modifier, dexterity_modifier, constitution_modifier, intelligence_modifier, wisdom_modifier, charisma_modifier  --  (integer value) *The default +/- for the skill, so a Race with 1 Strength gets +1 strength ot their roll.* 
- race_size  --  (integer value) *The default size of the race* 
- speed  --  (integer value) *The speed of the race* 
- default_languages  -- (list value) *The langauges that this race knows by default, for example: Undercommon, or Elvish, this is in addition to Common which is given to all races.* 
- number_of_bonus_languages  -- (integer value) *Number of additional languages a player can choose to take, this may also be DM's discretion.  Not a super important field.* 
- default_feats -- (list value) *The feats that this race gets at Level 1*
- feat_options -- (list value) *The additional feats the race can choose from*
- number_of_feat_choices -- (integer value) *the number of feats from feat_options that the player can choose.  This number should be less than the feat_options.*
- proficiencies -- (list value) *any and all proficiencies that the race has*
- number_of_bonus_proficiencies -- (integer value) *The number of bonus proficiencies that the player can choose from*
- number_of_bonus_modifiers -- (integer value) *The number of bonus modifiers that the player can choose from*

[IMAGE EXAMPLE](https://i.imgur.com/EljMyKZ.png)
