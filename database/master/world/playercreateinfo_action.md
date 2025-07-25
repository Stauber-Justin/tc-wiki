---
title: playercreateinfo_action
description:
published: true
date: 2023-10-22T16:06:29.318Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:34:23.529Z
---

<a href="https://trinitycore.info/en/database/master/world/playercreateinfo" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'playercreateinfo'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/playercreateinfo_cast_spell" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'playercreateinfo_cast_spell'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment |
| --- | --- | --- | :---: | :---: | --- | --- | --- |
| [race](#race) | tinyint | unsigned | PRI | NO | 0 |  |  |
| [class](#class) | tinyint | unsigned | PRI | NO | 0 |  |  |
| [button](#button) | smallint | unsigned | PRI | NO | 0 |  |  |
| [action](#action-alt) | int | unsigned |  | NO | 0 |  |  |
| [type](#type) | smallint | unsigned |  | NO | 0 |  |  |
&nbsp;
## Description of fields

### race
The character's [ChrRace ID](https://wago.tools/db2/chrraces)
| ID | Name      |
|----|-----------|
|  1 | Human     |
|  2 | Orc       |
|  3 | Dwarf     |
|  4 | Night Elf |
|  5 | Undead    |
|  6 | Tauren    |
|  7 | Gnome     |
|  8 | Troll     |
| 10 | Blood Elf |
| 11 | Draenei   |
{.dense}

&nbsp;

### class
The character's [ChrClass ID](https://wago.tools/db2/chrclasses)
| ID | Name         |
|----|--------------|
|  1 | Warrior      |
|  2 | Paladin      |
|  3 | Hunter       |
|  4 | Rogue        |
|  5 | Priest       |
|  6 | Death Knight |
|  7 | Shaman       |
|  8 | Mage         |
|  9 | Warlock      |
| 11 | Druid        |
{.dense}

&nbsp;

### button
The ID of the slot on the action bar where the action icon will be placed.
Special bars are used for stances, auras, pets, stealth, and other similar special modes.
|Button IDs | Set (key) | Comment |
|-----------|-----------|---------|
| 0-11 | 1 (SHIFT + 1) |  |
| 12-23 | 2 (SHIFT + 2) |  |
| 24-35 | 3 (SHIFT + 3) | Right Side Bar |
| 36-47 | 4 (SHIFT + 4) | Right Side Bar 2 |
| 48-59 | 5 (SHIFT + 5) | Bottom Right Bar |
| 60-71 | 6 (SHIFT + 6) | Bottom Left Bar |
| 72-83 | 1 SpecialA |  |
| 84-95 | 1 SpecialB |  |
| 96-107 | 1 SpecialC |  |
| 108-119 | 1 SpecialD |  |
{.dense}

&nbsp;

### action <!-- {#action-alt} -->
Depending on the **type** value:
* type = 0: [Spell ID](https://wago.tools/db2/spell)
* type = 128: [item entry](../world/item_template#entry) (yes item prototype, not item instance)
* type = 64: macro id
&nbsp;

### type
The type of action:
* 0: Spell
* 64: Macro
* 128: Item
&nbsp;

<a href="https://trinitycore.info/en/database/master/world/playercreateinfo" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'playercreateinfo'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/playercreateinfo_cast_spell" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'playercreateinfo_cast_spell'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
