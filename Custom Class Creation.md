# How to create custom classes
## KEY

**string value** - Can be anything you want, but generally alphanumeric.
- ex: class_name:Zyborg

**integer value** - Is 0-9 values (do not put alphanumeric in here or the command will fail)
- ex: hp:30
- ex:number_of_bonus_languages:1

**list value** - Can be anything you want, but this field accepts multiple inputs in a list, so **separate each item/thing with a semicolon (;) character.**
- ex: saving_throws:Str;Con
- ex: weapon_proficiencies:Short Bow;Short Sword

## COMMAND /customclasscreation
- class_name - (string value) *This is the name of the custom class, and will appear in the class selection list* 
Performance, Persuasion, Religion, SleightOfHand, Stealth, Survival
- hp - (integer value) *The default health the class starts with*
- saving_throws - (list value) *The default saving throws for this class*  **MUST BE FROM THE BELOW LIST:**
  - Str, Dex, Con, Int, Wis, Cha
- choices - (integer value) *the number of skill choices from the skills list*
- skills - (list value) *The skills that the class can select from* **MUST BE FROM THE BELOW LIST:**
  - Acrobatics, AnimalHandling, Arcana, Athletics, Deception, History, Insight, Intimidation, Investigation, Medicine, Nature, Perception, 
- feats - (list value) *The default feats the class gets*
- weapon_proficiencies - (list value) *The default weapon proficiencies of the class*
- armor_proficiencies - (list value) *The default armor proficiencies of the class*
- tool_proficiencies - (list value) *The default tool proficiencies of the class*
- starter_equipment - (list value) *The default equipment the class starts with*
- spellcaster (OPTIONAL) - (string value) *The spellcaster type of the class - Cha/Wis/Int for Spell Attack modifier*
- number_of_cantrips (OPTIONAL) - (integer value) *The number of cantrips the class knows at level 1*
- number_of_spells (OPTIONAL) - (integer value) *The number of spells the class knows at level 1*

[EXAMPLE 1](https://i.imgur.com/D3ZX4wN.png)
[EXAMPLE 2](https://i.imgur.com/4gVmj4T.png)
