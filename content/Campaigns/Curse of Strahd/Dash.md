

```dataview
TABLE
    hp as "Max HP",
    current_hp as "Current HP",
    round(currentEHP / maxEHP * 100) + "%" as "Vitality",
    choice(currentEHP / maxEHP < 0.3, "❌ CRITICAL", choice(currentEHP / maxEHP < 0.6, "⚠️ LOW", "✅ HEALTHY")) as "Status"
FROM "Campaigns/Curse of Strahd/Player Characters"
FLATTEN (
    default(current_hp, hp) + 
    (default(hit_d6, 0) * 4.5) + 
    (default(hit_d8, 0) * 5.5) + 
    (default(hit_d10, 0) * 6.5) + 
    (default(hit_d12, 0) * 7.5)
) as currentEHP
FLATTEN (
    default(hp, 0) + 
    (default(max_hit_d6, 0) * 4.5) + 
    (default(max_hit_d8, 0) * 5.5) + 
    (default(max_hit_d10, 0) * 6.5) + 
    (default(max_hit_d12, 0) * 7.5)
) as maxEHP
WHERE hp != null
SORT hp ASC
```

---

## 🌤️ Daytime Random Encounters — Barovia

**Encounter Roll:** `dice:1d12+1d8`

| Roll | Encounter |
|-----:|----------|
| 2 | `dice:3d6` [[statblock:Commoner]] |
| 3 | `dice:1d6` [[statblock:Scout]] |
| 4 | Hunting trap |
| 5 | Grave |
| 6 | False trail |
| 7 | `dice:1d4+1` [[statblock:Bandit]] |
| 8 | Skeletal rider |
| 9 | Trinket |
| 10 | Hidden bundle |
| 11 | `dice:1d4` [[statblock:Swarm of Ravens]] (50%) **or** [[statblock:Wereraven]] (raven form, 50%) |
| 12 | `dice:1d6` [[statblock:Dire Wolf]] |
| 13 | `dice:3d6` [[statblock:Wolf]] |
| 14 | `dice:1d4` [[statblock:Berserker]] |
| 15 | Corpse |
| 16 | `dice:1d6` [[statblock:Werewolf]] (human form) |
| 17 | 1 [[statblock:Druid]] with `dice:2d6` [[statblock:Twig Blight]] |
| 18 | `dice:2d4` [[statblock:Needle Blight]] |
| 19 | `dice:1d6` [[statblock:Scarecrow]] |
| 20 | 1 [[statblock:Revenant]] |

---

## 🌙 Nighttime Random Encounters — Barovia

**Encounter Roll:** `dice:1d12+1d8`

| Roll | Encounter |
|-----:|----------|
| 2 | 1 [[statblock:Ghost]] |
| 3 | Hunting trap |
| 4 | Grave |
| 5 | Trinket |
| 6 | Corpse |
| 7 | Hidden bundle |
| 8 | Skeletal rider |
| 9 | `dice:1d8` [[statblock:Swarm of Bats]] |
| 10 | `dice:1d6` [[statblock:Dire Wolf]] |
| 11 | `dice:3d6` [[statblock:Wolf]] |
| 12 | `dice:1d4` [[statblock:Berserker]] |
| 13 | 1 [[statblock:Druid]] with `dice:2d6` [[statblock:Twig Blight]] |
| 14 | `dice:2d4` [[statblock:Needle Blight]] |
| 15 | `dice:1d6` [[statblock:Werewolf]] (wolf form) |
| 16 | `dice:3d6` [[statblock:Zombie]] |
| 17 | `dice:1d6` [[statblock:Scarecrow]] |
| 18 | `dice:1d8` [[statblock:Zombie]] (Strahd variant) |
| 19 | 1 [[statblock:Will-o'-Wisp]] |
| 20 | 1 [[statblock:Revenant]] |
