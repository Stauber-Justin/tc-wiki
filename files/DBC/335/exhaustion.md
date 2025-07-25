---
title: Exhaustion.dbc
description:
published: true
date: 2023-09-30CEST01:03:36.000Z
tags: dbc, database client, 3.3.5, 3.3.5a, 335, 335a, wotlk
editor: markdown
dateCreated: 2023-08-09CEST00:06:01.000Z
---
<a href="https://trinitycore.info/files/DBC/335/environmentaldamage" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'EnvironmentalDamage'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/DBC" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to DBCs (3.3.5a)</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/faction" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'Faction'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

# Exhaustion.dbc
##### :pencil: Structure on [wowdev.wiki](https://wowdev.wiki/DB/Exhaustion)
&nbsp;

> :x: denotes unused fields
{.is-info}


## Structure

| Index | Field | Type | Reference |
| :---: | --- | :---: | --- |
| 0 | [ID](#id-alt) | uint32 |  |
| 1 | [XP](#xp) | int32 |  |
| 2 | [Factor](#factor) | float |  |
| 3 | [OutdoorHours](#outdoorhours) | float  |  |
| 4 | [InnHours](#innhours) | float  |  |
| 5 | [Name_0](#name-alt) | string |  |
| 6 | [Name_1](#name-alt) | string |  |
| 7 | [Name_2](#name-alt) | string |  |
| 8 | [Name_3](#name-alt) | string |  |
| 9 | [Name_4](#name-alt) | string |  |
| 10 | [Name_5](#name-alt) | string |  |
| 11 | [Name_6](#name-alt) | string |  |
| 12 | [Name_7](#name-alt) | string |  |
| 13 | [Name_8](#name-alt) | string |  |
| 14 | [Name_9](#name-alt) | string |  |
| 15 | [Name_10](#name-alt) | string |  |
| 16 | [Name_11](#name-alt) | string |  |
| 17 | [Name_12](#name-alt) | string |  |
| 18 | [Name_13](#name-alt) | string |  |
| 19 | [Name_14](#name-alt) | string |  |
| 20 | [Name_15](#name-alt) | string |  |
| 21 | [Name_lang_mask](#name-alt) | uint32 |  |
| 22 | [Threshold](#id-alt) | float  |  |
&nbsp;
## Description of fields

### ID <!-- {#id-alt} -->
:x: <code>Col: 0 (uint32)</code>

*- no description -*
&nbsp;

### XP
:x: <code>Col: 1 (int32)</code>

*- no description -*
&nbsp;

### Factor
:x: <code>Col: 2 (float)</code>

Rate EXP is earned in this state.
&nbsp;

### OutdoorHours
:x: <code>Col: 3 (float)</code>

*- no description -*
&nbsp;

### InnHours
:x: <code>Col: 4 (float)</code>

*- no description -*
&nbsp;

### Name <!-- {#name-alt} -->
:x: <code>Col: 5 &ndash; 21 ([Loc](/how-to/localization))</code>

*- no description -*
&nbsp;

### Threshold
:x: <code>Col: 22 (float)</code>

Rested has a value of 12. All else 0.
&nbsp;

<a href="https://trinitycore.info/files/DBC/335/environmentaldamage" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'EnvironmentalDamage'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/DBC" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to DBCs (3.3.5a)</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/faction" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'Faction'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
