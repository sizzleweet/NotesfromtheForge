---
Name: z_NPCTemplate
Type: NPC
Role: "Head Mechanic"
Callsign: 
Disposition: Friendly
FirstLook: "disgruntled, oppressed, but healthy"
Goal: "Bring peace to the universe"
RevealedAspect: "Really Quite Tender"
Difficulty: Dangerous
InProgress: true
Bond: false
Location:
  Sector: z_SectorTemplate
  Planet: z_PlanetTemplate
  Settlement: z_SettlementTemplate
obsidianUIMode: preview
---
# `=this.name` Details

- Their name is **`=this.Name`**.

- They go by **`=default(this.callsign,"their name, what else would you call them?")`**

- **`=this.Name`** is located in **`=link(this.Location.Settlement)`** on **`=link(this.Location.Planet)`**

- Their role is: **`=this.Role`** 
 
- They look: **`=this.FirstLook`.**

- Their disposition is **`=this.Disposition`**

- I know their goal is to: **`= this.goal`**

- As I've gotten to know them I've found out that they are: **`= this.RevealedAspect`**

# Notes

This is my BOND!  AND MY BOND IS MY WORD!!!


# Progress - `=this.Difficulty`

![[progress-track-0.svg]]

**`=choice(this.bond, "We have a strong bond", "We have no bond")`**
