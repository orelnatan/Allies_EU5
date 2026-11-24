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


Roadmap: the middle panel

1. Create WBP_AbilityButton in Content/UI: a single command button with the names the template expects, styled like your current slots.

2. Event-graph only step: in WBP_AbilityButton, add an OnAbilityButtonClicked event dispatcher fired by the button's OnClicked, and a small SetIcon
function.

3. Create WBP_CommandPanel in Content/UI with parent class UnitWidgetSelector, and lay it out in the Designer:

o 12 WBP_AbilityButton named AbilityButtonWidget_@ to AbilityButtonWidget_11;

+ and - page buttons;

o the four required widgets;

o one SelectButtonWidget_0, so the panel doesn't hide itself.

4. Event-graph only step: in WBP_CommandPanel:

o the Update event sets the 12 icons and tooltips;

o each button click calls ActivateKeyboardAbilitiesOnMultipleUnits;

o the page buttons call AddAbilityIndex;

0 CurrentAbilityButton calls OnCurrentAbilityButtonClicked.

5. In the Designer of WBP_ControlBar, place WBP_CommandPanel in the middle (CommandGrid) section, and collapse (don't delete) the old Border slots so the old
functions still compile.

6. Event-graph only step: register the HUD the template's way:

0 remove CreateWidget and AddToViewport from BP_RTSCameraPawn's BeginPlay;

o in WBP_ControlBar's PreConstruct, cast the player pawn to ExtendedCameraBase and call SetUnitSelectorWidget (WBP_CommandPanel).

7. In BP_RTSPlayerController Class Defaults, add WBP_ControlBar as element 0 of MainHUDs.

8. Play test: