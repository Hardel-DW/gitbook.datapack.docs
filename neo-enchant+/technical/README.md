---
description: >-
  This page explains the various configuration files of the NeoEnchant datapack
  and how they can be customized to fit your needs.
icon: microchip
---

# Technical&#x20;

## <mark style="color:orange;">Introduction</mark>

View the linked pages to see available modifications for block or entity lists. For example, if you want to change which blocks Bedrock Breaker can't break, these resources provide the necessary guidance.

[block-configuration.md](block-configuration.md "mention")

[entity-configuration.md](entity-configuration.md "mention")

***

## <mark style="color:orange;">Modifying Enchantments in NeoEnchant</mark>

This sections explains how to modify enchantment files to balance them according to your preferences.

### Where to Find Enchantment Files

Enchantment files are located in the `data/enchantplus/enchantment/` directory, organized by the type of item they apply to:

* `armor/` - Enchantments for all armor pieces
* `helmet/`, `chestplate/`, `leggings/`, `boots/` - Specific armor pieces
* `sword/`, `bow/`, `trident/`, `mace/` - Weapon enchantments
* `pickaxe/`, `axe/`, `hoe/` - Tool enchantments
* `elytra/` - Elytra-specific enchantments
* `mounted/` - Mount equipment enchantments
* `tools/` - General tool enchantments
* `durability/` - Durability-related enchantments

### Understanding Enchantment Files

Enchantment files are in JSON format and contain several important sections, json is a format that's easy to understand, look at.

<details>

<summary>Enchantment JSON Content</summary>

```json
{
    "description": {
        "translate": "enchantment.enchantplus.name",
        "fallback": "Display Name"
    },
    "exclusive_set": "#enchantplus:exclusive_set/group",
    "supported_items": "#minecraft:enchantable/item_type",
    "weight": 8,              // Rarity (higher = more common)
    "max_level": 5,           // Maximum enchantment level
    "min_cost": {             // Minimum enchanting table cost
        "base": 9,
        "per_level_above_first": 9
    },
    "max_cost": {             // Maximum enchanting table cost
        "base": 21,
        "per_level_above_first": 11
    },
    "anvil_cost": 1,          // Additional anvil cost
    "slots": ["slot_type"],   // Where the enchantment works
    "effects": {              // What the enchantment does
        // Effect definitions...
    }
}
```

</details>

### Example with Life+

The Life+ enchantment (`armor/lifeplus.json`) adds extra health to the player. By default, it adds 2 health points (1 heart) per level. And the Content.  Here's an example of how to increase the number of hearts per level.

<details>

<summary>Life+ JSON</summary>

```json
{
	"description": {
		"translate": "enchantment.enchantplus.lifeplus",
		"fallback": "Life+"
	},
	"exclusive_set": "#enchantplus:exclusive_set/armor",
	"supported_items": "#minecraft:enchantable/armor",
	"weight": 8,
	"max_level": 5,
	"min_cost": {
		"base": 9,
		"per_level_above_first": 9
	},
	"max_cost": {
		"base": 21,
		"per_level_above_first": 11
	},
	"anvil_cost": 1,
	"slots": ["armor"],
	"effects": {
		"minecraft:attributes": [
			{
				"id": "minecraft:enchantment.lifeplus",
				"attribute": "minecraft:max_health",
				"amount": {
					"type": "minecraft:linear",
					"base": 2,
					"per_level_above_first": 2
				},
				"operation": "add_value"
			}
		]
	}
}

```

</details>

{% stepper %}
{% step %}
### Open the .zip/jar

Open the contents of the datapack, or extract it with Windows 11 or Winrar. (For Mac/Linux I don't know)

{% hint style="info" %}
For the jar, I recommend editing without unzipping the jar
{% endhint %}
{% endstep %}

{% step %}
### Locate

Go to the file at `data/enchantplus/enchantment/armor/lifeplus.json` and open it with the editor of your choice
{% endstep %}

{% step %}
### Find the value to replace

Find the `effects` section and change the `base` and `per_level_above_first` values from `2` to `4`:

* The first named `base` indicates the value at level 1
* The second named `per_level_above_first` indicates the value to add for each level.
{% endstep %}

{% step %}
### Save and it's done !

All that's left to do is save and we're done.  Transform it into a zip file, don't forget to restart your world !

{% hint style="info" %}
making sure to select the “data and pack.mcmeta” folder. if you zip the parent folder, it won't be any good.
{% endhint %}
{% endstep %}
{% endstepper %}





***



