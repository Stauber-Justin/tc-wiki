---
title: TalentTab.dbc
description:
published: true
date: 2023-10-07T22:12:20.541Z
tags: 3.3.5, 3.3.5a, 335, 335a, wotlk, dbc, database client
editor: markdown
dateCreated: 2023-10-04T08:08:33.366Z
---

<a href="https://trinitycore.info/files/DBC/335/talent" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'Talent'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/DBC" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to DBCs (3.3.5a)</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/taxinodes" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'TaxiNodes'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

# TalentTab.dbc
##### :pencil: Structure on [wowdev.wiki](https://wowdev.wiki/DB/TalentTab)
&nbsp;

> :x: denotes unused fields
{.is-info}


## Structure

| Index | Field | Type | Reference |
| :---: | --- | :---: | --- |
| 0 | [ID](#id-alt) | uint32 |  |
| 1 | [Name_0](#name-alt) | string |  |
| 2 | [Name_1](#name-alt) | string |  |
| 3 | [Name_2](#name-alt) | string |  |
| 4 | [Name_3](#name-alt) | string |  |
| 5 | [Name_4](#name-alt) | string |  |
| 6 | [Name_5](#name-alt) | string |  |
| 7 | [Name_6](#name-alt) | string |  |
| 8 | [Name_7](#name-alt) | string |  |
| 9 | [Name_8](#name-alt) | string |  |
| 10 | [Name_9](#name-alt) | string |  |
| 11 | [Name_10](#name-alt) | string |  |
| 12 | [Name_11](#name-alt) | string |  |
| 13 | [Name_12](#name-alt) | string |  |
| 14 | [Name_13](#name-alt) | string |  |
| 15 | [Name_14](#name-alt) | string |  |
| 16 | [Name_15](#name-alt) | string |  |
| 17 | [Name_lang_mask](#name-alt) | uint32 |  |
| 18 | [SpellIconID](#spelliconid) | unit32 | [SpellIcon.dbc/0](/files/DBC/335/spellicon#id-alt) |
| 19 | [RaceMask](#racemask) | uint32 | [ChrRaces.dbc/0](/files/DBC/335/chrraces#id-alt) |
| 20 | [ClassMask](#classmask) | uint32 | [ChrClasses.dbc/0](/files/DBC/335/chrclasses#id-alt) |
| 21 | [PetTalentMask](#pettalentmask) | uint32 | [CreatureFamily.dbc/8](/files/DBC/335/creaturefamily#pettalenttype) |
| 22 | [OrderIndex](#orderindex) | uint32 |  |
| 23 | [BackgroundFile](#backgroundfile) | string |  |
&nbsp;
## Description of fields

### ID <!-- {#id-alt} -->
<code>Col: 0 (uint32)</code>

*- no description -*
&nbsp;

### Name <!-- {#name-alt} -->
:x: <code>Col: 1 &ndash; 17 ([Loc](/how-to/localization))</code>

*- no description -*
&nbsp;

### SpellIconID
:x: <code>Col: 18 (unit32)</code>

*- no description -*
&nbsp;

### RaceMask
:x: <code>Col: 19 (uint32)</code>

| Value | Flag   | Name      |  | Value | Flag   | Name      |
|-------|--------|-----------|--|-------|--------|-----------|
|     1 | 0x0001 | Human     |  |     2 | 0x0002 | Orc       |
|     4 | 0x0004 | Dwarf     |  |    16 | 0x0010 | Undead    |
|     8 | 0x0008 | Night Elf |  |    32 | 0x0020 | Tauren    |
|    64 | 0x0040 | Gnome     |  |   128 | 0x0080 | Troll     |
|  1024 | 0x0400 | Draenei   |  |   512 | 0x0200 | Blood Elf |
|  1101 | 0x044D | *_Alliance_* |  |   690 | 0x02B2 | *_Horde_* |
{.dense}

0 for pets
&nbsp;

### ClassMask
<code>Col: 20 (uint32)</code>

| Value | Flag   | Name      |  | Value | Flag   | Name         |
|-------|--------|-----------|--|-------|--------|--------------|
|     1 | 0x0001 | Warrior   |  |    32 | 0x0020 | Death Knight |
|     2 | 0x0002 | Paladin   |  |    64 | 0x0040 | Shaman       |
|     4 | 0x0004 | Hunter    |  |   128 | 0x0080 | Mage         |
|     8 | 0x0008 | Rogue     |  |   256 | 0x0100 | Warlock      |
|    16 | 0x0010 | Priest    |  |  1024 | 0x0400 | Druid        |
{.dense}

0 for pets
&nbsp;

### PetTalentMask
<code>Col: 21 (uint32)</code>

Its a bit mask: `1 << PetTalentType`

0 for player chars
&nbsp;

### OrderIndex
<code>Col: 22 (uint32)</code>

*- no description -*
&nbsp;

### BackgroundFile
:x: <code>Col: 23 (string)</code>

`interface\talentframe\*`
&nbsp;

<a href="https://trinitycore.info/files/DBC/335/talent" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'Talent'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/DBC" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to DBCs (3.3.5a)</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/taxinodes" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'TaxiNodes'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
