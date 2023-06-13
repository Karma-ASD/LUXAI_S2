# LUXAI_S2
LUXAI season 2 bronze solution
## A SIMPLE RULE BASED AGENT
### Early Phase:
In the Early Phase, a bid (≥ 0) is entered for a new factory, a faction is declared, and the factories are placed onto the player's side of the map. A simple early_setup function is written to return the appropriate action for handling this phase. At timestep 0, a bid is placed in addition to declaring a faction (this is something that will be used for the official release and will not affect gameplay at any time). Each unit of bidding removes 1 water and 1 metal from the starting pool of water and metal. N factories are given to each team to place, with the winning bidder (if there is one) receiving N+1 factories. For the next N+1 steps, both teams are allowed to place factories anywhere on their own half.

### Regular Phase:
In early regular phase, bots with certain functions are declared and generated, light and heavy based on the resources available.
In most cases:
1 heavy bot for ice extraction
4 light bot for ore extraction
4 light bot for rubble extraction
0 kill bots since require loads of resource and donot make a difference down the line
Upto 300 steps, ice & ore bots are used for extraction and maintaining a crucial state in early game i.e being an invader and defending an invasion.
After 300 upto 800 steps, rubble bots are produced. Combined efforts of rubble and ore bots is used to clean the nearest rubble and defend from an invasion.

### End Phase:
After 800 step, ore bots become invaders and self destructors. In late game they self destruct on oponent lichens to produce rubble. 
Subsequently lichens are produced in factories leading to higher demand of water which is balanced by a simple additive bias function.
