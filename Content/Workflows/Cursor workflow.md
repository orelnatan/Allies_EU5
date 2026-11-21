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
1. Create four Gameplay Ability blueprints, one per USA building, and set each Ability Icon to that building's thumbnail.

2. On BP_Caterpillar_D7_Dozer, add those four abilities to Default Abilities, in this order: Command Center, Barracks, War Factory,
Supply Center.

3. Event-graph only step. In Content/UI/WBP_ControlBar, fill CommandSlot_0 onward from the focused unit's Default Abilities, and
clear every unused slot while leaving the cell in place.

4. Press Play, select the dozer, and confirm those four thumbnails show from the right. Click empty ground and confirm the
command cells clear without shifting.