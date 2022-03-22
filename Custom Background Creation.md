
# How to create custom backgrounds

## KEY

**string value** - Can be anything you want, but generally alphanumeric. 
- ex: race_name:Zyborg

**integer value** - Is 0-9 values (do not put alphanumeric in here or the command will fail) 
- ex: race_size:30 
- ex:number_of_bonus_languages:1

**list value** - Can be anything you want, but this field accepts multiple inputs in a list, so **separate each item/thing with a semicolon (;) character.** 
- ex: saving_throws:Str;Con 
- ex: default_skills:Athletics;Arcana;Deception;Insight

## COMMAND /custombackgroundcreation
- background_name - (string value) *This is the name of the custom background, and will appear in the background selection list*
- default_skills - (list value) *The default skills that the background is proficient in, **MUST BE FROM THE BELOW LIST:**
  - Acrobatics, AnimalHandling, Arcana, Athletics, Deception, History, Insight, Intimidation, Investigation, Medicine, Nature, Perception, Performance, Persuasion, Religion, SleightOfHand, Stealth, Survival
- languages - (list value) *Default languages the background knows*
- bonus_any_languages - (integer value) *How many additional languages the player can select*
- starting_tools - (list value) *The starting tools the background gets*
- starting_equipment - (list value) *The starting equipment the background gets*
- gold_coins - (integer value) *The number of gold coins the player starts with*

[IMAGE EXAMPLE](https://i.imgur.com/ZbstloA.png)
