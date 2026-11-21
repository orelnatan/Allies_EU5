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
1. On BP_Caterpillar_D7_Dozer, set Unit Icon to Caterpillar_D7_Dozer_Thumbnail.

2. Event-graph only step. In Content/UI/WBP_ControlBar, drive PortraitSlot from SelectedUnits at
CurrentUnitWidgetIndex, using that unit's Unit Icon.

3. Press Play, select the dozer, and confirm PortraitSlot shows the dozer thumbnail. Deselect it and confirm the slot
clears.

4. Set Unit Icon the same way on the other units and buildings that already have a _Thumbnail texture: Sherman, GMC
truck, US Supply Center, US Barracks, US Command Center, US War Factory.

5. Press Play, box-select the dozer together with a Sherman, and confirm the portrait shows the Sherman.