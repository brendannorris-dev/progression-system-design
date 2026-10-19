# Progression & Data Tracking in Non-Linear Systems
Case study mapping modular progression system and persistent state logic modeled on a non-linear tabletop RPG campaign


## Design Challenge & Goal
This system design case study stems from a homebrew tabletop roleplaying campaign engineered to heighten player agency and maintain structural narrative pacing. The primary goal was to create a structure that allowed players to experience multiple genres and character classes. The core challenge lay in balancing non-linear exploration with a cohesive narrative story.

## System Architecture
The system splits progression into two distinct acts. Act 1 utilizes four independent narrative arcs that take place concurrently across the global timeline. Operating like a state machine, the system prompts players to choose a route from the main hub that they have yet to complete. Global counter tracks progress (routes_completed) until they hit the conditional state to trigger the transition into Act 2.

## Data Persistence & Player Agency
Players choices should hold meaningful weight across these tracks, so the system implements data persistence. Critical narrative decisions and major story elements are captured in boolean tracked variables (e.g. train_stolen = True). Throughout the Act 1 loop, these variables are stored globally; after completion of all four routes, these variables are input into the Act 2 setup - altering starting conditions, relationships, and unlocking new potential story elements.
