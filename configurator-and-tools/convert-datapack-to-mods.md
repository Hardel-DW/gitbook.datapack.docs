---
icon: box-open
---

# Convert Datapack to Mods

## <mark style="color:orange;">Datapack to Mod Converter</mark>

### Introduction

Our versatile conversion tool allows you to effortlessly transform almost any Minecraft datapack into a functional Fabric/Forge/Quilt/Neo Forge mod.&#x20;

The process is designed to be simple, typically requiring just a few clicks via its user interface.

{% embed url="https://voxel.hardel.io/en-us/tools/converter" %}

### How It Works

Fundamentally, many Minecraft Fabric/Forge... mods consist of up to three main components:&#x20;

* A datapack,&#x20;
* A resource pack
* And Java code files. However, the Java code is optional; a mod can function perfectly well containing only the datapack and/or resource pack elements.

Our converter takes your existing datapack (.zip) and repackages it into the .jar format expected by Fabric/Forge. It automatically adds the necessary metadata files required by the mod loader (such as fabric.mod.json).&#x20;

Essentially, the core content remains your original datapack, just wrapped within a mod file structure.

### Are Performance Characteristics Different?

No. Since the converter primarily repackages your existing datapack files, the performance characteristics remain identical.&#x20;

Whether you load your content as a standalone datapack or as the converted mod, Minecraft handles the underlying data (recipes, functions, structures, etc.) in exactly the same way.
