---
obsidianUIMode: preview
---

# Intro

Hey all, this is my attempt at hacking together a bunch of other peoples stuff (see: [[LICENSE]]) and making my own version of an obsidian vault for Starforged play.

My goal here was to make this game as streamlined as possible while still allowing for hands on and analog play.  The whole project started because I wanted to create info and lore for the world I'm building (totally optional, obviously).  So for me, I like fill out little info sheets about things like the different ship sizes and factions and whatever else I find interesting that I'd like to document somewhere.  I normally do that in a Lore folder... but obviously feel free to do whatever you would like with this project.

I've broken the readme up into two different sections. 
 - [[#How to use this vault|First]] is a quick walkthrough of starting up a new campaign.
 - [[#How to specifically use this vault|Second]] is a little more detail on how to use the vault while playing as well as some details on the mechanics of it all.


# How to use this vault

- So the first thing I'd do is to check out this readme... Ok cool done.
- For real though... Here are the steps I would take to start a brand new campaign.
- THIS IS VERY IMPORTANT... DON'T CHANGE PREWRITTEN THINGS IN THE DETAILS SECTION.... I mean unless you want to, I'm just saying that the details are reliant on the front matter.
	- It's all populated by the front matter.  You might need to click off and back on the document for the actual page to refresh.
	- You can add anything you want or remove whatever you want (obviously) but the intent is that the frontmatter is where most of the details about the places/people go.
- ANOTHER IMPORTANT THING:
	- Front matter names need to be exact.
	- If you use spaces put "quotes" around the value.
	- For ease of use and continuity I'd recommend matching the filename to the Frontmatter name.
- One last thing, front matter only shows up in editing mode.  Once you're done editing something you can change the last line in the front matter from `source` to `preview` from then on the note will open in reading view for a more pleasant experience.  I also HIGHLY recommend learning some basic Hotkeys (in this instance it's ctrl/cmd+E to switch between reading and editing mode)

## 1. Character Setup
- Next I'd start with my character.  You can start in the `1.2 Character` folder.
- Fill out the Truths file [[3. Character Truths]]
- Fill out the front matter and anything else you've got in the character note: [[1. Character Main]]
- Then I'd go ahead and set up my [[CharacterSheetDrawing]].
- From there, I'd move to Assets.  Set them up by adding them to the [[AssetDrawing]]
	- remember to add an image to an excalidraw drawing, hold CTRL(win) (or Shift for MAC) while dragging from the folders into the drawing.
	- Anything in the dotted boxes will show up in [[2. Character Assets]]

## 2. Location Setup
- Next up Locations and NPC.
- Alright so start off in the `3. Locations` folder

### Build your planets 
`~/3. Locations/2. Planets`
- Right click duplicate the template file.
- Fill out all the front matter you have.  Any notes etc.
- Add an image (optional)

### Build Your settlement 
`~/3. Locations/3. Settlements/`
- Right click duplicate the template file.
- Fill out all the front matter you have.  Any notes etc.
- Add an image (optional)

### Build your Sector!
`~/3. Locations/1. Sector/`
**Remember... Hold Ctrl/Cmd when dragging an image in from the folders to a drawing.**
- This is the fun one!
- Either create a new drawing or make a duplicate of the template
- Add a Background Image (optional) and then lock it.
- Add images from the `~/z_Support/Images/Space`
- Give the images links
	- Right click and then add "Create Link". Type in the asset you're referencing.

 
## 3. NPC Setup
`~/2. NPCs/`
- Copy the template.
- Fill out front matter.

## 4. Profit?



# How to specifically use this vault

## Journal Entry Example
[[z_NPCTemplate]] and I went down to watering hole on [[z_PlanetTemplate]].  There we had a wonderful time.  But alas, it was time for us to get back to [[Z_SettlementTemplate]].  Oh well.  Next time I'm in the [[z_SectorTemplate]] sector, I'll have to do some stuff.

We were driving a bit erratically on the way back home.

> [!success]- [[4. Moves/Scene_Challenge/Face_Danger|Face_Danger]]: Iron + 0
> ![[d6-6-t.svg#invert_W|50]]![[plus-t.svg#invert_W|15]]![[stat-1-t.svg#invert_W|50]]![[plus-t.svg#invert_W|15]]![[add-0-t.svg#invert_W|50]]![[equals-t.svg#invert_W|15]]![[total-7-t.svg#invert_W|50]]
> ![[vs-t.svg#invert_W|50]]![[d10-5-t.svg#invert_W|50]]![[and-t.svg#invert_W|50]]![[d10-3-t.svg#invert_W|50]]
> ### Result: ![[outcome-strong-hit.svg|50]] Strong Hit

### Move instructions
The command for moves is a bit wonky here's the premise
	`;;move [[MoveName]]" StatNAME StatValue Addvalue::`
Once you type in your brackets it'll come up with a list of all the items start typing your move name and seletct it from the asset list

Here's the syntax I used for roll above
	`;;move [[Face_Danger]] Iron 3 0::`


You can also use your own number if you're playing with analog dice by adding three numbers at the end in this format **d6,d10,d10**

For example:
	`;;move [[MoveName]] heart 1 4 6,10,10::`
###


SO ANYWAYS... We made it safely.

BUT... Damnit this wasn't what I wanted for this example so we'll still pay the price.


> [!tip] Pay the Price:  *You are harmed*


### Pay the price Details
- This command is easy as heck... `;;ptp::`
	- It will return the nice looking callout for you to do what you want with it.
### 


Back to the narrative:  OH wait... yeah that's right we made it safely but also we were harmed.... :D

### Oracle Roller

- One last thing is that you can roll on any oracle using the dice roller command.  
	- See the plugin instructions for details. 
	- Basically it's a `` `dice: [[tablename#^tableid]]` ``) 
	- If you want the dice roll to be persistent on the page (HIGHLY RECOMMENDED) use this syntax `` `dice-mod: [[tablename#^tableid]]` ``.   Adding dice mod actually modifies the markdown with the results.
		- This is my preferred method especially in journals and location/npc sheets.
	- I personally haven't had much luck with the saving of global rolls option.

## How to use the Character Sheet

- The template version of the character sheet is located here: [[charactersheet1.svg]]
- The example character sheet in the `~/1.2 Character/` folder is an excalidraw file.  
	- I have locked the main picture in place
	- The red blocks around it are movable.
	- The asset cards are from `~/z_Support/AssetCards/`
- You can create a separate excalidraw drawing for the asset cards if you'd like, I just have those main ones there because They seem relevant to the character.
- The excalidraw image is fully editable and you can also capture images from within the drawing and display them based on selection.  Check here:
## Assets

- All asset cards are located in the folder: `z_Support/AssetCards`
- I personally play with physical cards so I just have these as reference.  I included an "asset card" drawing to kind of simulate a way to play with them digitally.
- There are a ton of ways to use the cards and the assets
## How to use the sector map

- The sector map is similar to the Character Sheet.  Uses excalidraw.
- All images for the sector maps are located here: `~/z_Support/Images/Space`
- By right clicking any object in excalidraw you can turn it into a link.

## Locations

- !! **Don't change anything in the details heading directly, instead edit the FrontMatter.** !!
- Locations are broken up into sectors, planets, and settlements.
- Each note has a template.
- For deep space settlements leave the planet key blank.
- The Location names need to be an exact match of the target Name key value in the FrontMatter.
	- For example:
		 -Settlement:
			```
			Name: Settlement1
			Location: "Planet 1"
			```  
		-Planet:
			```
			Name: "Planet 1"
			```
## NPCs

- !! **Don't change anything in the details heading directly, instead edit the FrontMatter.** !!
- NPC's follow similar rules as the Locations.  FrontMatter values for locations must be exact matches.
- Marking progress is manual (for now).  You can find all 40 variations of progress here in this folder: `~z_Support/Images/z_Progress/ProgressTracks`
- I find it easier to just increment the tag manually by editing it and changing the value to however many ticks you want.






# Still to do:

- Add all the oracles to the mix.  I'll eventually have them all in there so you can roll on them in your journal or whatever.
- I want to create a first look NPC, planet, settlement generator like in stargazer
- Play the game at some point... that'd be neat too.
=======

>>>>>>> d22fb614a04d5df403097e43239f4230868d020f
