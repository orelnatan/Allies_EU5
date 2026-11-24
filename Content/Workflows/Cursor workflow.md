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

1. In Content/Bases, create GA_BuildBuilding_Base, a project-owned build ability with parent
GameplayAbilityBase. Add the WorkAreaClass and ConstructionUnitClass variables and set its Class
Defaults.

2. Event-graph only step: in GA_BuildBuilding_Base, rebuild the template's build logic without the debug
prints. When the ability activates, it commits. When the cursor hit arrives, it checks that the team can afford
it, then spawns the ghost (SpawnWorkAreaReplicated) and ends the ability. If the team can't afford it, it plays
a failure sound and ends the ability.

3. In the Command Center folder, create BP_WorkArea_US_Command_Center with parent WorkArea. This is the
ghost actor: it uses the Command Center mesh with the template's transparent blue material, red when the
spot isn't allowed, and its BuildingClass is BP_US_Command_Center.

4. Reparent GA_Build_US_Command_Center to GA_BuildBuilding_Base, then set its Class Defaults:
WorkAreaClass, ConstructionUnitClass, and ConstructionCost.

5. Event-graph only step: in GA_Build_US_Command_Center, delete the two empty events (Event
ActivateAbility and Event OnEndAbility). Otherwise they'd override the parent's logic and nothing would
happen.

6. Play test: select the Dozer and click the Command Center button. The ghost should follow the cursor. Left-
click places it, and the Dozer should drive over and build. Right-click cancels.