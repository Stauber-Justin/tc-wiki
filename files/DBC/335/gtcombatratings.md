---
title: GtCombatRatings.dbc
description:
published: true
date: 2023-09-30CEST01:03:36.000Z
tags: dbc, database client, 3.3.5, 3.3.5a, 335, 335a, wotlk
editor: markdown
dateCreated: 2023-08-09CEST00:06:01.000Z
---
<a href="https://trinitycore.info/files/DBC/335/gtchancetospellcritbase" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'GtChanceToSpellCritBase'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/DBC" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to DBCs (3.3.5a)</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/gtnpcmanacostscaler" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'GtNPCManaCostScaler'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

# GtCombatRatings.dbc
##### :pencil: Structure on [wowdev.wiki](https://wowdev.wiki/DB/GtCombatRatings)
&nbsp;

> Game Table:
> This dbc file is not indexed, but **Data** is stored in a fixed order.
> Entries: 100 x 32 (see [GameTables](/files/DBC/335/gametables) data)
{.is-info}

> :x: denotes unused fields
{.is-info}


## Structure

| Index | Field | Type | Reference |
| :---: | --- | :---: | --- |
| 0 | [Data](#data) | float |  |
&nbsp;
## Description of fields

### Data
<code>Col: 0 (float)</code>

CombatRating required for 1% effect. (pending other modifiers)

[`enum CombatRating`](https://github.com/TrinityCore/TrinityCore/blob/3.3.5/src/server/game/Entities/Unit/Unit.h#L319-L346)
| ID | Name |
|----|------|
| 0 | CR_WEAPON_SKILL |
| 1 | CR_DEFENSE_SKILL |
| 2 | CR_DODGE |
| 3 | CR_PARRY |
| 4 | CR_BLOCK |
| 5 | CR_HIT_MELEE |
| 6 | CR_HIT_RANGED |
| 7 | CR_HIT_SPELL |
| 8 | CR_CRIT_MELEE |
| 9 | CR_CRIT_RANGED |
| 10 | CR_CRIT_SPELL |
| 11 | CR_HIT_TAKEN_MELEE |
| 12 | CR_HIT_TAKEN_RANGED |
| 13 | CR_HIT_TAKEN_SPELL |
| 14 | CR_CRIT_TAKEN_MELEE |
| 15 | CR_CRIT_TAKEN_RANGED |
| 16 | CR_CRIT_TAKEN_SPELL |
| 17 | CR_HASTE_MELEE |
| 18 | CR_HASTE_RANGED |
| 19 | CR_HASTE_SPELL |
| 20 | CR_WEAPON_SKILL_MAINHAND |
| 21 | CR_WEAPON_SKILL_OFFHAND |
| 22 | CR_WEAPON_SKILL_RANGED |
| 23 | CR_EXPERTISE |
| 24 | CR_ARMOR_PENETRATION |
{.dense}

Ordered by combat rating, character level 1 &ndash; 100 ASC.
`idx = (RatingID * 100) + (level - 1)`
&nbsp;

<a href="https://trinitycore.info/files/DBC/335/gtchancetospellcritbase" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'GtChanceToSpellCritBase'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/DBC" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to DBCs (3.3.5a)</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/files/DBC/335/gtnpcmanacostscaler" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'GtNPCManaCostScaler'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
