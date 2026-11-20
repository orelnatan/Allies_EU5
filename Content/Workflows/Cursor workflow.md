Our workflow:

Please give me the step-by-step flow... do not move to the next step until I am done with the current step.

And about event graphs...
I have found that event graphs cost me a lot of time... so make sure to include a "step" specifically for event graphs...example:

First, show a "Roadmap" - Please write the roadmap as a regular list with numbers, not as a table.

step 1
do this and do this and do this...

step 2
do this and do this and do this...

step 3 - an event-graph **only step
here we need an event-graph in the file: BP_RTSPlayerController...

step 4 
do this and do this and do this...

step 5 - an event-graph **only step
here we need an event-graph in the file: BP_Glados..

step 6
do this and do this and do this...

Than, show step 1...

etc...


This way, I can switch you to agent mode and tell you to implement steps 3 and 5... The goal of this approach is that I don't waste time on the event graphs... Please make sure the event graphs are isolated with their own steps, so you can take it from there under agent mode...

Thank you from advanced



Roadmap

1. Open BP_Caterpillar_D7_Dozer and confirm it is a child of BP_VehicleUnitBase, with tripo_part_0
through tripo_part_10 visible on the capsule.

2. On that same Blueprint, set the team, the Al controller, and the capsule so a click can hit it and a move
order has a controller to run.

3. Place one dozer on Tropical Island, sitting on the ground inside the green navigation area.

4. Make the level's Player Start team match the dozer. Team 0 is the spectator, and a spectator can select a
unit and cannot order it to move. Confirm the level's GameMode is BP_RTSGameMode.

5. Press Play on Tropical Island. Left-click the dozer, then right-click the ground. It should draw a move
marker and drive there.

