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

Roadmap
1. In Content/Bases/Materials, create the master material M_BuildingGhost and set its main properties in the
Details panel (translucent, lit). No nodes yet.

2. Graph-only step: in M_BuildingGhost, build the node graph. It has texture parameters (BaseColor, Normal,
Roughness, Metallic), an Opacity scalar, and the red-floor logic: Invalid, InvalidColor and FloorHeight.
The floor logic compares each pixel's height above the actor's pivot and tints the bottom band red when
Invalid is 1.

3. In the Command Center folder, create two material instances of M_BuildingGhost:
MI_Ghost_US_CommandCenter (Invalid = 0) and MI_Ghost_US_CommandCenter_Invalid (Invalid = 1). Plug in
the Command Center textures and tune Opacity.

4. In BP WorkArea_US_Command_Center, set the Mesh's slot 0 material to MI_Ghost_US_CommandCenter. Set

TemporaryHighlightMaterial to MI_Ghost_US_CommandCenter_Invalid, and clear OriginalMaterial (or set it
to the valid instance). Then adjust HighlightDuration if needed. OriginalMaterial matters because your
Blueprint currently has a value saved there. If it still points at the blue material, the ghost would flip back to
blue every time the red flash ends.

5. Play test: select the Dozer and click the Command Center button. The ghost should look like the real building
but see-through. Over a blocked spot (no-build zone, overlapping building, enemy unit), its floor should turn
red. After you drop it, check how the construction site looks while the Dozer builds.