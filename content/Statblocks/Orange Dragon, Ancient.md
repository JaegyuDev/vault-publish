---
type: Dragon
subtype: Water
size: Gargantuan
movements:
  - Swimming
  - Flying
languages:
  - Draconic
cliamte: Tropical
terrain:
  - Forest
  - Rivers
  - Lakes
---
```statblock
layout: Basic 5e Layout
name: Ancient Orange Dragon
size: Gargantuan
type: dragon
alignment: neutral evil
ac: 23
hp: 462
hit_dice: 25d20 + 200
speed: "40 ft., fly 90 ft., swim 40 ft."
stats: [28, 16, 26, 16, 15, 19]
saves:
  - dexterity: 10
  - constitution: 15
  - wisdom: 9
  - charisma: 11
skillsaves:
  - perception: 16
  - stealth: 10
damage_immunities: "fire"
damage_resistances: "poison"
condition_immunities: "poisoned"
senses: "blindsight 60 ft., darkvision 120 ft., passive Perception 16"
languages: "Draconic"
cr: 22
traits:
  - name: "Legendary Resistance (3/Day)"
    desc: "If the dragon fails a saving throw, it can choose to succeed instead."
actions:
  - name: "Multiattack"
    desc: "The dragon can use its Frightful Presence. It then makes three attacks: one with its bite and two with its claws."
  - name: "Bite"
    desc: "Melee Weapon Attack: +16 to hit, reach 15 ft., one creature. Hit: 25 (3d10 + 9) piercing damage."
  - name: "Claw"
    desc: "Melee Weapon Attack: +16 to hit, reach 10 ft., one creature. Hit: 22 (3d8 + 9) slashing damage."
  - name: "Tail"
    desc: "Melee Weapon Attack: +16 to hit, reach 20 ft., one creature. Hit: 20 (2d10 + 9) bludgeoning damage."
  - name: "Frightful Presence"
    desc: "Each creature of the dragon's choice within 120 feet and aware of it must succeed on a DC 20 Wisdom saving throw or become frightened for 1 minute. Repeat the save at the end of each turn; immunity for 24 hours on success."
  - name: "Sodium Breath (Recharge 5-6)"
    desc: "The dragon exhales liquid sodium in a 60-foot line, 5 feet wide. Water causes explosions dealing 38 (7d10) fire damage within 15 feet (DC 22 Dex save for half). Creatures coated in sodium ignite next turn for 82 (15d10) fire damage. Water contact causes immediate explosion; the primary victim automatically fails."
legendary_actions:
  - name: "Detect"
    desc: "The dragon makes a Wisdom (Perception) check."
  - name: "Tail Attack"
    desc: "The dragon makes a tail attack."
  - name: "Wing Attack (Costs 2 Actions)"
    desc: "Each creature within 15 ft. must succeed on a DC 20 Dexterity saving throw or take 13 (2d6 + 6) bludgeoning damage and be knocked prone. The dragon can then fly up to half its flying speed."

```