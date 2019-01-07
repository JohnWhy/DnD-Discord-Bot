# !r Guide
## !r - is a pretty complex command, with a lot of different features.  This guide will help to explain them.

+ Let's start basic.
 * !r1d20 - This will roll a 20 sided dice.
 * !r2d20 - This will roll 2 20 sided dice.
 * !r1d6 - This will roll a 6 sided dice.
 * !r5d1000 - This will roll 5 1000 sided dice.  You can roll up to 25 dice, and those dice can have as many sides as you want.

+ Let's add in some modifiers
 * !r1d20+2 - This will roll a 20 sided dice and add 2 to it.
 * !r2d20+2 - This will roll 2 20 sided dice and then add 2 to the sum of each of them.  So if you roll a 10 and an 11, you will get 21+2=23.
 * !r1d20 + Acrobatics - This will roll 1 20 sided dice and add in your Acrobatics. (case insensitive)
 * !r1d20 + str - This will roll 1 20 sided dice and add in your Strength modifier. (case insensitive)

+ Now let's roll multiple dice, but only keep highest and lowest
 * !r5d20kh1 - This will roll 5 20 sided dice, and keep the highest 1.  It will still display all 5, but the top will clearly state which one is highest.
 * !r25d8kl2 - This will roll 25 8 sided dice, and keep the lowest 2.
 * *kh and kl can be remembered as "keep highest" and "keep lowest".*

+ You can also kh and kl, alongside modifiers
 * !r2d20kh1 + acrobatics - This will roll 2 20 sided dice, and keep the highest one, then add in the acrobatics skill to that highest roll.
 * !r2d20kh1 + 5 - This will roll 2 20 sided dice, keep the highest one, then add 5 to the highest roll.
 * !r5d8kl3 + str - This will roll 5 8 sided dice, keep the lowest 3, sum them up, then add the strength modifier.

+ This about sums it up, feel free to play around with this command and find what works best for you.  

## Thank you to numerous people for suggestions about how I can improve the roll command.

