
![Creature Genetics](https://raw.githubusercontent.com/meldurson/Creature_Genetics/main/Pics/Banner.png)
**Bring true genetics and selective breeding to Valheim.**

Creature Genetics gives every creature its own unique genetic code that determines its physical attributes and offspring. Instead of every animal being identical, each creature is born with randomized DNA that is inherited through breeding, allowing you to create stronger bloodlines over generations.


## 💎Features

* 🧬 Every creature has unique DNA generated when it is created.
* ❤️ Genetic variation within:  

| Trait     | Description | Default Range | 
| ----------- | ----------- | ----------- | 
| Health      | Multiplies the amount of health   | 0.1x-2x   
| Armour      | Reduces the amount of damage taken    | 0.2x-5x   
| Speed      | Multiplies the movement speed   | 0.01x-2x   
| Size    | Multiplies the size of a creature   | 0.25x-2x*   
| Productivity    | Reduces time taken to breed  | 0.6x-3x*   
| Drops    | Multiples the dropped loot  | 0.6x-3x*   
| Color    | Changes color using RGB values  | N/A  

\*Range can be modified in the configuration files


* 👶 Offspring inherit DNA from both parents with natural variation, allowing selective breeding and long-term improvement.
* 🦌 Cross-species breeding support (or male and female).
* ⚙️ Fully configurable breeding pairs through an easy-to-edit `.yml` file.
* 🔄 Existing creatures automatically receive DNA when first encountered.
* 💾 Genetic data is permanently saved with each creature.

## 🦠Cross-Species Breeding

Using the included configuration file, you can define entirely new breeding combinations between creatures. For example, you can allow the different types of Fuelings to breed with eachother or make it so only Fueling Shamans can breed and give a chance to have any of the three as an offspring.

The breeding system is driven by a YAML configuration, making it easy for modpacks and server owners to customize without modifying the mod itself.

## 🐦‍🔥Compatibility

DNA Genetics has been designed to work alongside popular creature mods and overhauls such as:


* Let Me Tame You
* Portable Pals
* CLLC (Creature Level and Loot Control)
* SLS (Star Level System)


## ⚙️Configuration

Most DNA settings can be customized through the generated __.cfg__ configuration file.

You can configure:

* Trait inheritance
* Trait ranges
* Mutation chances



### For cross-breeding
Creature-specific breeding behavior

It uses the .yml format. When you run the mod it creates a __CreatureGenetics_DefaultGeneticsList.yml__

You can have multiple genetics list files in your config folder. They just need to be in the format of: *CreatureGenetics_\*.yml* where the * can be anything. 

An example is __CreatureGenetics_Monstrum.yml__ if you want to add genetics for Monstrum creatures. 

### Examples:

The general format for this list is as follows
```yaml
PrefabName:
  MatePrefabName:
    Offspring1: Chance out of 100
    Offspring2: Chance out of 100
  MatePrefabName2:
  MatePrefabName_etc:
  canMateWithSelf: true or false
```
Below is an example of having Fueling Shaman only able to breed with Fueling Berserker and have an option of offspring of any Fueling
```yaml
GoblinShaman:
  GoblinBrute:
    GoblinBrute: 25
    Goblin: 50
  canMateWithSelf: false

GoblinBrute:
  canMateWithSelf: false
```
* shaman can only breed with a brute
* brute cannot have offspring
* The offspring is a 25% chance of brute, 50% chance of goblin
* since this is less than 100%, the remaining is 25% chance of shaman

If you want to have any number of creatures be able to breed with eachother you can just add them to a line separated by commas "," and ending with a colon ":" such as all the different Dverger
```yaml
Dverger,DvergerMage,DvergerMageFire,DvergerMageIce,DvergerMageSupport,DvergerAshlands:
  ```


## 🤝Designed for Modpacks

DNA Genetics is intended to be a foundation for creature progression rather than a complete overhaul. It integrates naturally with existing gameplay and works well alongside mods that add new tameable creatures.

Whether you're building the perfect wolf pack, breeding giant boars, or perfect breeding resource farms ,every generation has the potential to improve.


## ❓Contact:
The most reliable way to reach out would be to ping me in the [Valheim Modding Discord](https://discord.com/invite/GUEBuCuAMz) under @Meldurson. or dm me on Discord.

If you want to support me you can do so through my Ko-fi account:

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/B0B3NARM0)


