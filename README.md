# SelectionBUG

This repo is meant to demonstrate the bug in AHUD::GetActorsInSelectionRectangle method from Unreal Engine, as of 4.25.3
Steps to reproduce:

1) Launch the Project in the editor
2) Start a PIE session
3) Press and hold the left mouse button to start a selection rectangle
4) Try to include the two cilinders (TestActors) inside the green selection rectangle that is drawn
5) Notice that another TestActor (TestActor OUTSIDE THE SCREEN) is always considered as part of the selection

All the relevant code is inside CustomHUD, plus two delegates on TopDownController and the corresponding input binding
