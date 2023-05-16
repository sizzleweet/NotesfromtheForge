---
Name: "z_SettlementTemplate"
Type: Settlement
SettlementType: Planetside   #Must be one of these types: Planetside, Orbital, DeepSpace
FirstLook: "was built from Natural Materials"
InitialContact: Neutral
Population: Hundreds 
Authority: Oppressive 
Projects: Archeology 
Trouble: "Betrayal from within, Ghostly Visitations"
Location: 
  Sector: "[[z_SectorTemplate]]"
  Planet: "[[z_PlanetTemplate]]"
obsidianUIMode: source
---
# `=this.name` Details

- It is `= choice(this.SettlementType="Orbital","an","a")` **`= this.SettlementType`** settlement
- This settlement is located `= choice(this.SettlementType="PlanetSide", "in the sector:",  "on the planet:")` `= default(link(this.Location.Planet), link(this.Location.Sector))`
- Upon Initial Inspection this settlement looks **`= this.FirstLook`**
- There are **`=this.Population`** of people being governed by an Authority that is **`=this.Authority`**
- I see that they are heavily involved in **`=this.Projects`**
- Seems they have a bit of trouble in the form of **`=this.Trouble`**

# NPCs
```dataview
TABLE WITHOUT ID file.link AS "Name", Location.Settlement AS Location
WHERE Location.Settlement = this.name AND Type="NPC"
```

# Notes

