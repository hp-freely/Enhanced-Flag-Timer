# Enhanced Flag Timer
A script that provides dedicated HUDs for tracking the time value (in seconds) since a flag was dropped for a given team.

### Summary
Enhanced Flag Timer (EnhancedFT) was built to serve two purposes:
1. Provide a configurable Flag Timer GUI HUD that can be managed through HUD Mover. Runar released the original FlagTimer script in 2001 which displayed a flag timer in the objective HUD. Since that time, I'm unaware of any other script that tried to iterate this. His script was very simple, and it works fine. However, given how large our screens are now, having to look at small font in the bottom left of the screen for critcal information doesn't make sense.
2. Provide a way to customize the flag timer start value for a given CTF game mode. There is no mechanism by which the client can reference the configured flag return time from the server. In other words, whatever is configured by the server is hidden to the client. As a result, we have to configure it manually. Runar's original script hard-coded a 45 second timer. Given the movement of the community to use a shorter timer for LCTF, this configuration now is necessary. 
 
With the above, this script combines the following items:
1. A complete redesign on how to manage flag timer data, making use of many of the new support /original classes. Almost nothing remains of the original Runar script.
2. A configurable GUI for showing flag timer data in a large font or small font.
3. A UI that allows you to configure the flag timer through the Lobby tab for the following modes: CTF, LCTF, Other (catch-all for other modes)
4. A UI that allows you to configure flag timer values *per server* for a given game mode. This is useful when different servers us different flag timers for the same game mode.
5. A mechanism for the script to detect the game mode dynamically.
6. Playing a warning sound when the friendly flag is about to return. This is useful when the defense is guarding the flag in the field. It can get quite hectic, and losing track of the return timer does occur.
