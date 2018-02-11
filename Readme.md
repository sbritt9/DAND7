# Storytelling with Data
## Author: Stephen Britton
## Date: Feb 2018

# Summary
The premise of this report is to explore the idea of the term, “power creep” and how it relates to the Nintendo mega-franchise known as Pokemon.  Pokemon serves as a good example for a franchise that is susceptible to power creep; this is because it spans over 7 iterations with new content being added each time.

Power creep occurs when new content is added to an existing game and the new content is designed in such a way that older content is made obsolete or inferior.  Because of the broad approach of power creep in video games, I chose to focus on a few key attributes of Pokemon that are shared across generations that have significant impacts to that Pokemon’s performance.

## Base Stats
The first marker for power creep will be one of the most obvious indications; base stat total.  Every pokemon has a myriad of stats that govern how the pokemon performs in battle, these stats are as follows:

* Attack: contributes to how much physical damage is output by a pokemon
* Defense: contributes to how much physical damage is received by a pokemon
* Special Attack: contributes to how much non-physical damage is output by a pokemon
* Special Defense: contributes to how much non-physical damage is received by a pokemon
* Speed: determines the order in which pokemon attack in battle
* HP: a numeric value that represents how much damage a pokemon can receive before “fainting” (being unable to battle)

By taking the average of the base stats then grouping them by generation, we will be able to determine if latter generations of pokemon have significantly greater sums of base stats making former pokemon less useful in battle.

## Same-Type Attack Bonus (STAB)
The second marker for power creep to be investigated will be Same-Type Attack Bonuses - or STAB for short.  Every pokemon and every attack is categorized by at least 1 type (fire, water, electric, grass, etc.), when an attack type matches with the pokemon type, there is an amplification to the damage output for that attack.  Because a pokemon can have up to 2 types (fire-rock, water-fighting, etc.), STAB bonus distribution may overlap further increasing, reducing or even negating damage amplification.

These STAB bonuses are represented numerically:

* A Fire type pokemon using a Water type move would receive a damage reduction and be represented as .5
* A Fire type pokemon using a Fire type attack would receive a damage increase and be represented as 2
* A Fire type pokemon using a Normal type attack would not receive any increase and would be represented as 1

Like the Base Stats, STAB bonus modifiers will be averaged and grouped by generation.  If there is an increasing trend in STAB bonuses there will be an increase in damage output by newer pokemon not found in older pokemon thus indicating power creep.

## Legendary Status
The final marker to be investigated is a little more complex than a strictly numeric feature.  This feature will indicate whether or not a pokemon is considered 'legendary'.  In the world of pokemon, there are some that are considered rare; this could be because they are hard to find, hard to catch, or both.  While rarity is important in filling out a collection, it generally does not impact a pokemon’s performance.  There are however, certain pokemon that are designed to be stronger than average, there are usually only one instance of each legendary pokemon per video game and are often hidden away and extremely difficult to catch.

Like the previous sections, grouping will be again based on generation; however, instead of averaging, sums will be evaluated across generations to see if the game developers have introduced more legendary pokemon in more recent games than in older games.  While not strictly a form of power creep, legendary pokemon are objectively stronger than non legendary pokemon and a having more in circulation can impact the usability of older pokemon. 

# Design
Because data is distilled across various generations of pokemon, comparative differences are very important to convey clearly.  Due to the numbers of Base Total and STAB Total being so close, bar charts would not be able to accurately represent the variance between them, rather, we will be using a line graph.  For the Legendary Status, a bar chart represents the gaps between generations well.

Normally, it is not appropriate to change the base of the y-axis from 0; however, because the margins between generations are so low, in order to see the trends in the visual representation, we need to be able to increase the minimum y-axis value.  To not represent this dishonestly, a slider will be provided that will change the base value of the y-axis for both base total and STAB total dynamically.

Since we are essentially performing unary analysis, visual encoding is implemented for aesthetics and attention direction with muted grays and bright blues.  To keep the visuals clean and uncluttered of information, hover effects are implemented to reveal numeric values of the bars and points on the graphs.

Basic instruction was not included in the original design in the graph; however, based on feedback, x-axis labels, y-axis labels, chart title and brief descriptions will be added.

# Feedback
"I would change the perspective of the narrative from 'we' to something more neutral.  In the last paragraph, it is not clear that you are talking about legendary pokemon, is it legendary and rare?  The graphs really need more description, I don't really understand what I'm looking at without any labels or words.  I would make the sliders more consistent between the last two graphs, also, it shouldn't move by such a little amount on the second graph.  The against-total needs to be better explained, it's a nice graph, but I don't understand it." - Anne Brinkman

"I like the graphs, but I feel like the report doesn't really come to an end.  I think it needs a conclusion or something that brings everything together." - Jonathon Britton

"This looks good, but the numbers are so long on the line graphs.  I think it is distracting to have numbers go across the graph like that.  It would be better if they were rounded off and would also look more polished.  I don't really know anything about pokemon so I only know what is written here, but I think that you break it down well enough to understand." - Ana Ferguson


# Resources

* Storytelling with Data by Cole Nussbaumer
* Interactive Data Visualization for the Web by Scott Murray
* https://www.kaggle.com/rounakbanik/pokemon - Kaggle Pokemon Dataset
* https://bl.ocks.org/d3noob/