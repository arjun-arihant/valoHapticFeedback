# Preliminary thougts on the methodology
there are multiple sub-projects in this project each can be completed individually
### Making a tracking software that finds the damage halo
Need to consider how the tracking should be carried out so there is minimal resource utilisation.
possible methods:
1. just track the complete circular region and extract the damage halo when it appears
2. ~~track for bullet sounds and activate it based on that~~ (too many variables, unnecessarily complicated)
3. track the heath and armour values, as soon as there is a change capture the damage halo (might cause delay)

In the 3rd option we can reduce the delay by capturing both the health value region and damage halo region.
Only analyse health and if health changes immideately capture halo from the already available capture.
Not sure, if I am doing this much already why not just extract the damage halo directly?
The only possible advantage is that there might be a chance of false positives due to enemy movement/ sprays etc.

--- 
### Analysing the halo to find the coordinates of damage
There are many ways of finding the coordinates, I think any can be used, there shouldn't be much of a difference.
Just make sure to also take into account when multiple source of damage are there.
Maybe blacklist the are where the initial damage was from?
NO it wont work for pistol shots I think
what if there is no new marker pressent just send coordinates of the previous marker?

---
### logic for the development board to use the coordinates to activate the motors
This should be quite easy. There can be a status file from which the board constantly reads data.
As soon as there is data board sends the command to the motors.
Maybe there is something even more easy and efficient? As I learn more about this I will come into contact with it.

---
>Will keep updating this as new ideas/inspirations/knowledge is gained.