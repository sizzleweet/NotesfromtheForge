---
Name: z_PlanetTemplate
Type: Planet
PlanetType: Furnace
Atmosphere: Breathable
Description: "A planet with relentless volcanic activity, wreathed in fire and ash"
ObservedFromSpace: "Firey world-spanning chasms, Towering mountain ranges"
PlanetSideFeatures: "Blinding ash storms, Lava tube tunnel networks"
Settlements: 1
Life: 
Location:
  Sector: "[[z_SectorTemplate]]"
obsidianUIMode: source
---
![[Furnace_01.png|center|300]]


# `=this.name`

- Located in the `=link(this.Location.Sector)` sector.
- This is a: **`= this.PlanetType`** planet
- The air is: **`= this.Atmosphere`**
- From space you can see: **`=this.ObservedFromSpace`**
- Once I got on the planet I saw: **`=this.PlanetSideFeatures`**
- There is: **`=default(this.Life,"no")` life** on this planet.

## Settlements
```dataview
TABLE WITHOUT ID file.link AS "Name", SettlementType AS "Type"
WHERE Location.Planet = this.Name AND Type = "Settlement"
```

## NPCs
```dataview
TABLE WITHOUT ID file.link AS "Name", Location.Settlement AS "Location"
WHERE Location.Planet = this.Name AND Type = "NPC"
```


## Notes


Here are some notes