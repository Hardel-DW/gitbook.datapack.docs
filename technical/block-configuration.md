# Block Configuration

## <mark style="color:orange;">Block Tags</mark>

Block tags allow you to customize lists of blocks that will be affected by specific enchantments. These tags are located in the `data/enchantplus/tags/block/` directory.

### How to Use Block Tags

Block tags are JSON files that define which blocks are affected by certain enchantments. You can:

* Add individual blocks by their ID (e.g., `"minecraft:stone"`)
* Reference existing block groups with the `#` prefix (e.g., `"#minecraft:logs"` to target all log blocks)
* Remove blocks by adding them in a "remove" section

***

### <mark style="color:orange;">Using Minecraft's Block Groups</mark>

When you see a `#` symbol before a value (like `"#minecraft:logs"`), it references a predefined group of blocks. This is a powerful feature that allows you to target entire categories of blocks without listing each one individually.

Example common block groups include:

* `#minecraft:logs` - All log blocks
* `#minecraft:planks` - All planks
* `#minecraft:ores` - All ore blocks

This makes configuration much simpler and ensures compatibility when new blocks are added to Minecraft in updates.

***

### <mark style="color:orange;">Available Block Tags</mark>

#### **Bedrock Breaker (`bedrock_breaker.json`)**

This tag defines blocks that can be broken by the Bedrock Breaker enchantment.

<details>

<summary>The current values</summary>

```json
{
    "values": [
        "minecraft:bedrock"
    ]
}
```

</details>

#### Timber (`timber.json`)

This tag defines the list of blocks that can be broken in chains by the Timber enchantment. Typically this includes logs, leaves, and mangrove roots.

<details>

<summary>The current values</summary>

```json
{
  "values": [
    "#minecraft:logs",
    "#minecraft:leaves",
    "minecraft:mangrove_roots"
  ]
}
```

</details>

#### Vein Miner (`veinminer.json`)

This tag defines the list of blocks that can be mined in veins using the Vein Miner enchantment. This typically includes all ore types in the game.

<details>

<summary>The current values</summary>

```json
{
    "values": [
        "minecraft:gold_ore",
        "minecraft:iron_ore",
        "minecraft:copper_ore",
        "minecraft:coal_ore",
        "minecraft:lapis_ore",
        "minecraft:diamond_ore",
        "minecraft:redstone_ore",
        "minecraft:emerald_ore",
        "minecraft:nether_quartz_ore",
        "minecraft:nether_gold_ore",
        "minecraft:deepslate_gold_ore",
        "minecraft:deepslate_iron_ore",
        "minecraft:deepslate_copper_ore",
        "minecraft:deepslate_coal_ore",
        "minecraft:deepslate_lapis_ore",
        "minecraft:deepslate_diamond_ore",
        "minecraft:deepslate_redstone_ore",
        "minecraft:deepslate_emerald_ore",
        "minecraft:ancient_debris"
    ]
}
```

</details>

#### **Mining Plus Blacklist (`miningplus.json`)**

This tag defines blocks that should NOT be affected by the Mining+ enchantment's 3x3 breaking effect. This protects valuable blocks and containers from being accidentally broken.

The list includes many blocks like:

* Containers (chests, barrels, etc.)
* Crafting stations (crafting table, furnace, etc.)
* Decorative elements (banners, beds, etc.)
* Special blocks (spawners, beacons, etc.)

<details>

<summary>The current values</summary>

```json
{
    "values": [
        "#minecraft:crops",
        "#minecraft:flowers",
        "#minecraft:saplings",
        "#minecraft:banners",
        "#minecraft:beds",
        "#minecraft:corals",
        "#minecraft:doors",
        "#minecraft:buttons",
        "#minecraft:signs",
        "#minecraft:fences",
        "#minecraft:fence_gates",
        "#minecraft:pressure_plates",
        "#minecraft:wool_carpets",
        "#minecraft:small_flowers",
        "#minecraft:candles",
        "#minecraft:replaceable",
        "#minecraft:dragon_immune",
        "minecraft:spawner",
        "minecraft:trial_spawner",
        "minecraft:vault",
        "minecraft:powder_snow",
        "minecraft:stonecutter",
        "minecraft:lectern",
        "minecraft:beehive",
        "minecraft:bee_nest",
        "minecraft:composter",
        "minecraft:conduit",
        "minecraft:ender_chest",
        "minecraft:barrel",
        "minecraft:chest",
        "#minecraft:shulker_boxes",
        "minecraft:trapped_chest",
        "minecraft:crafting_table",
        "minecraft:furnace",
        "minecraft:blast_furnace",
        "minecraft:smithing_table",
        "minecraft:smoker",
        "minecraft:brewing_stand",
        "minecraft:enchanting_table",
        "minecraft:anvil",
        "minecraft:grindstone",
        "minecraft:note_block",
        "minecraft:jukebox",
        "minecraft:lodestone",
        "minecraft:bell",
        "minecraft:beacon",
        "minecraft:flower_pot",
        "minecraft:loom",
        "minecraft:cartography_table",
        "minecraft:lantern",
        "minecraft:soul_lantern",
        "minecraft:soul_torch",
        "minecraft:torch",
        "minecraft:wall_torch",
        "minecraft:redstone_torch",
        "minecraft:campfire",
        "minecraft:soul_campfire",
        "minecraft:redstone_wire",
        "minecraft:tripwire",
        "minecraft:tripwire_hook",
        "minecraft:lever"
    ]
}
```

</details>

####
