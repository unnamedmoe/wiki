---
title: Chat Commands
description: Available Chat Commands, these are used with the "!" bang prefix
published: true
date: 2023-02-28T23:32:34.538Z
tags: admin, squad, chat commands, commands
editor: markdown
dateCreated: 2023-02-28T23:32:31.323Z
---

# Chat Commands for Admins and Players
Battlemetrics allows us to utilize commands, these are tools that you can use in-game to do actions or broadcast messages.

## General Player Commands Available
Players have access to the following commands, and their basic function 

- `!profile` provides link to the user profile based on `/profile` used in discord 
- `!onlyfans` provides patreon information
- `!admin` reports to admins 
- `!rules` displays rules locations
- `!discord` displays discord link 
- `!switch` switches player, this has a 15 minute trigger lock
- `!commands` ^ ^ displays above ^ ^ 
- `!stuck` switches player twice, this has a 15 minute trigger lock

## Server Profile Linking System
To facilitate automation, we have moved to [Squad Whitelister](https://github.com/fantinodavide/Squad_Whitelister)

Our Squad server runs the "Profile" link system, this ties your discord account (& roles) to your squad player account.

## Statistics
These are only available in the discord, and can be utilized with /stats. 
These stats are available to anyone, utilizing /stats requires /profile for it to be linked. 

# Admin Only Commands
All Commands in this subset are to be used by administration staff. If the category marked by `User Commands` then all users (players) can utilize.
## Map Voting
#### User Commands

-   `!vote help`  - sends possbile commands to a player in the from of a warning
-   `!vote choices`  - sends choices to player in the from of a warning
-   `!vote results`  - sends player the results in a warning

#### [](https://github.com/fantinodavide/squad-js-map-vote#admin-commands)Admin Commands

-   `!vote start`  - Starts a vote with 6 layers, random modes
-   `!vote cancel`  - Cancels current round of voting
-   `!vote cancelauto`  - Cancel scheduled automatic start of vote
-   `!vote end`  - Gently ends the current vote and announces the winner layer
-   `!vote restart`  - Restarts voting with 6 random maps and modes
-   `!vote broadcast`  - Broadcasts current voting results - happens every 7m automatically

##### [](https://github.com/fantinodavide/squad-js-map-vote#vote-by-modes)Vote by modes

-   `!vote start *_raas`  - Starts a vote with 6 layers, all RAAS
-   `!vote start *_aas`  - Starts a vote with 6 layers, all AAS
-   `!vote start *_inv`  - Starts a vote with 6 layers, all INV

##### [](https://github.com/fantinodavide/squad-js-map-vote#vote-by-map)Vote by map

-   `!vote start yeh gor lash gor albas`  - Starts a vote with X maps, random modes

##### [](https://github.com/fantinodavide/squad-js-map-vote#vote-by-map--mode-mixed)Vote by map + mode, mixed

-   `!vote start yeh_raas gor_raas lash_inv gor albas_inv`  - Starts a vote with X maps, X modes

## Admin Chat Commands
- `!seedrules` No weaponized emplacements allowed while seeding! Refer to the server rules for more info. Do not fob hunt! Do not move radio location in seeding. Avoid building Tarp/Camo net Buildings please.
- `!live` The server is now live! Please play out the map, and the next map will roll quickly! Thanks for seeding, visit us at theunnamedcorp.com
- `!tarps` While in seeding, please do not build observation towers, or hasco bunkers completely near central point. These tarped buildings are not fun for everyone, and can cause negative user feedback. Thank you for understanding
- `!thanksseed` Thanks for helping us seed! Visit theunnamedcorp.com if you want to become a regular, and gain whitelist!
- `!seedlink` Thank you for helping us seed! If you connect your profile on our Discord to your Steam ID, you can gain seeding rewards for playing here! beunnamed.com
#### User Commands
- `!seeding` *Warns Player*
	- While on a seeding map, please do not build observation towers, hasco bunkers, weaponized emplacements.
	- Fight over the middle points during seeding!
	- View our rules on our website or discord
## Admin Notifcation System
The [Admin notification](https://www.battlemetrics.com/rcon/triggers/edit/a826fadf-f4b0-4101-b111-da2e0cb4b2c4) system is a battlemetrics, squadJS triggers system utilized to alert administrators to a players request

#### Automated Messages [cont'd]
 - If the player utilizes `!admin` and does not reflect continued wording [exact match], then the player will be warned with a response to add wording

## Server Rules Automation and Chat Enforcement

Server Rules are available in the Message of the Day, on the [Unnamed Website](http://theunnamedcorp.com/squad.html#sqserverrules) and in our [Discord](https://discord.com/channels/836985182778556436/1063890894455054426). *Players have no excuse to not find our rules.*

For our most convuluded rules, here are some more enhanced admin direction these following incident types.
### Claims Enforcement 
Our squad utilizes squad claims to manage team cohesion. Many servers run first-come-first-served basis, **we are not one of them.**
#### Chat Commands
- `!claims`  Responds with three global chat responses based on [trigger](https://www.battlemetrics.com/rcon/triggers/edit/bd3cb7e7-7e9c-43a5-8946-f0bf5363bd07)
	- Vehicles are done by Squad Names! Please read our rules at: theunnamedcorp.com. First named squad has priority. Discord has a list of all acceptable names.
	- Squads must be named after the vehicle name/type, and can claim multiple of the SAME assets (example LAV-25 can claim 2x LAV-25 if 6 crew, TANK = Tank Squad, etc.) 
	- Squads named "ARMOR" have no claims here and are forbidden, please utilize 1 vehicle type only. 
- `!dual` Squads can not claim 2 different vehicle types. Ex: Bradley/Tank

To prevent "Armor" / "Vehicle" squads, the server has a built in [validation service](https://github.com/fantinodavide/squadjs-squad-name-validator)
- Admins can view the log of squad name validations [here](https://discord.com/channels/836985182778556436/1064237320435400726) for any failed responses
- The following is the current regex schema
```regex
/(a ?r ?m ?(?:o|e)? ?u? ?r)|(v ?i ?c)|(v ?e ?h ?i ?c ?l ?e)/gi
```
> A Robust Vehicle Squad Name Listing is available [here](https://discord.com/channels/836985182778556436/1063890894455054426) 


## Main Camping
Main camping is always a hard topic to deal with, our rules allow for **complete admin discretion** when managing the main camping enforcement rule. It is a good rule of thumb, that if something is not really meant to be there based on game objectives, then they are most likely main camping. 

Rules state that "engaging enemies within an approximate "450m" from their main is considered main camping. This however cannot apply for all maps, therefore your discretion is paramount. 

First step is to "Warn" the player, either verbally or through the in-game warning system. 

#### To Warn a Player utilizing an Automated Flagging System (AFS)
1. Press Servers, select our [server](https://www.battlemetrics.com/rcon/servers/16023606) 
2. Select the Player Name, press the arrow 
3. Select "Main Camping" 
4. You will be asked to confirm the main camp warning, and the server will execute the following warning to the player 
- `Camping enemy mains is not allowed! Please remove yourself, and all deployed assets`
- `Failure to comply, will result in removal`
- Execute Player Flag Added > Main Camp 

#### Chat Command
- `!main` triggers two global chat responses
	- Main Base Camping is defined as positioning assets, infantry, or mines, at any distance, with the intent to destroy enemy assets entering or leaving main. 
	- We deal with Main Base Camping on our server on a case-by-case basis. Admin discretion is final, if there are issues or disagreements, bring them to discord.
- `!minemain` Do not mine, or camp the enemy main! Play the objective!!!

## Teamplay Enforcement
Playing an objective is the main part of squad, it's pretty much the reason for the games existence. To play as a squad  in a group of squads. 

What defines `Teamplay` can be open to interpretation, but here in our server we are looking for the following things: 
1. Supporting an Active Objective, whether it's on RAAS, or Invasion through defending, or attacking those selected points on the map via the in-game system. 
2. Supporting their team through logistical actions 
3. Supporting their team through distanced based armor support
4. Supporting their team through setting up mortar fobs 
5. Supporting their team that is in any justifiable way supporting their team, it's pretty obvious

#### What Isn't Teamplay 

6. Actively pushing off the flag into areas way off the main objective 
7. Camping mains 
8. Taking a full squad of 9+ guys into nowhere to go "Fob Hunting" or actively play off objectives, with some dumb flank scheme that makes no sense 
9. TOW Fobs with a full squad of 9 people for essentially what is 1 asset by 1 person. 
Use your discretion, we have an Auto Flag for Teamplay that tells the player `Your team needs you! Please play active objectives!` 

### Chat Commands
- `!teamplay` prompts two global chat messages 
	- This is a teamplay server, follow objectives, communicate, play together. Listen to your commander.
	- Failure to abide by this, can result in your removal.
- `!ptfo` Play the ACTIVE objective!!

## Squad Leaders
Either the most beneficial or damning thing to a team are squad leaders. 

**Our squad leaders must:**
1. Have a microphone 
2. Have a squad leader kit 
3. Must not lead a free kit squad, which essentially means no direction - "DO WHATEVER YOU WANT" 

### Chat Commands
- `!sl` Squad Leads must have a Squad Leader Kit, Microphone. They must lead their squad.
- `!lead` prompts two global chat messages 
	- You must lead the squad you create, lock the squad at appropriate players for your assets if necessary. 
	- Squads that are not being led, and utilized as a free kit squad will be disbanded.

## General Chat Commands for Admins
- `!afk` 

> All players must join a squad, or will be considered AFK and kicked
> for active players!

- `!tk` 

> Apologize for your Teamkills in All-Chat! [J] Failure to do so, can
> result in removal.

- `!int` 

> Intentional teamkilling of any kind is not tolerated, do not teamkill
> intentionally.

- `!toxic` 

> Toxic behavior will not be tolerated - be respectful to all players on
> the server

- `!language` 

> Abusive Language / Hate Speech is NOT Tolerated, you will be banned.

- `!politics` 

> Please do not discuss politics or other controversial topics in chat!

- `!clearchat` 

> Clear the Global Chat!

- `!ls` 

> No Locked squads under 4 unless named task such as LOGI, VEHICLE_NAME, HELI
> You must unlock your squad when asked by an Admin

- `!ram` 

> No Ramming With Helicopters, or their blades. You will be removed.

- `!bait` 

> Creating a squad you do not intend to lead leads to removal from our
> server. If your squad leader left, please either find a leader or
> disband the squad.

- `!ticket` 

> Do not share ticket info in all chat!

- `!submit` 

> If you are reporting abusive behavior, submit all evidence to our
> discord to expedite the process

- `!ghosting` 

> Ghosting is sharing information to the other team, do not share
> information intentionally. If you are caught sharing information, you
> will be permanently banned.

- `!solo` 

> Do not solo vehicles that require crewman kits to operate!

### Advertising 

- `!clan` 

> Are you a clan looking for a community to call home? Head to our
> discord today, talk to an admin about group whitelisting.

- `!thankyou` 

> Thank you for playing here! Hit up our community at
> theunnamedcorp.com! Feedback welcome!

- `!joindiscord` 

> Join our community today! discord.gg/unnamedcorp! Giveaways,
> Whitelist, Gaming Community, Maplesyrup pics.

- `!recruiting` 

> We're recruiting! Stop by our website at beunnamed.com!

- `!afterparty` 

> Join / Visit our community at beunnamed.com!

- `!enjoy` 

> Enjoying our server? Hop on our discord! Be apart of the community and
> gain whitelist! beunnamed.com

- `!whitelist` 

> Wanting to have a whitelisted slot? Head to our website for more info.
> theunnamedcorp.com

- `!fwl` 

> Do you SL or Command often?! We take note! You can get free whitelist,
> join our discord to learn more.