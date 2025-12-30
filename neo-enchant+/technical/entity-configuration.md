---
description: >-
  Entity type tags define which entities are affected (or not affected) by
  certain enchantments. These tags are located in the
  data/enchantplus/tags/entity_type/ directory.
---

# Entity Configuration

### <mark style="color:orange;">How Entity Type Tags Work</mark>

Entity type tags are JSON files that specify lists of entities that should be included or excluded from certain enchantment effects. They work similarly to block tags but apply to living entities, projectiles, and other in-game objects.

You can:

* Include specific entity types by their ID (e.g., `"minecraft:cow"`)
* Reference groups of entities using the `#` prefix (e.g., `"#minecraft:aquatic"`)
* Exclude entities from existing groups

***

### <mark style="color:orange;">Entity Groups with</mark>

Like with block tags, the `#` prefix references predefined groups of entities:

* `#minecraft:aquatic` - Water-dwelling entities like fish and dolphins
* `#minecraft:arrows` - All arrow projectiles
* `#voxel:boat` - All types of boats
* `#voxel:minecart` - All types of minecarts
* `#voxel:non_living` - Non-living entities like item frames and paintings
* `#voxel:projectile` - All projectile entities (arrows, tridents, etc.)

***

### <mark style="color:orange;">Available Entity Type Tags</mark>

#### Last Hope Blacklist (`last_hope_blacklist.json`)

Defines entities that cannot be targeted by the Last Hope enchantment. This tag prevents the enchantment from being used against certain entities, such as players.

<details>

<summary>The current values</summary>

```json
{
    "values": [
        "minecraft:player"
    ]
}
```

</details>

#### Rebound Blacklist (`rebound_blacklist.json`)

Defines entities that arrows with the Rebound enchantment cannot bounce off. This prevents the enchanted arrows from interacting with certain entity types.

<details>

<summary>The current values</summary>

```json
{
    "replace": false,
    "values": [
        "#minecraft:aquatic",
        "#minecraft:arrows",
        "#voxel:boat",
        "#voxel:dev",
        "#voxel:minecart",
        "#voxel:non_living",
        "#voxel:projectile",
        "minecraft:player"
    ]
}
```

</details>

#### Telluric Blacklist (`teluric_blacklist.json`)

Defines entities that cannot be affected by the Telluric Wave enchantment. This prevents the seismic wave effect from affecting certain entity types.

<details>

<summary>The current values</summary>

```json
{
    "replace": false,
    "values": [
        "#minecraft:aquatic",
        "#minecraft:arrows",
        "#voxel:boat",
        "#voxel:dev",
        "#voxel:minecart",
        "#voxel:non_living",
        "#voxel:projectile",
        "minecraft:player"
    ]
}
```

</details>
