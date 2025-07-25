---
title: creature_template_addon
description:
published: true
date: 2024-02-17T07:28:48.420Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:30:18.868Z
---

<a href="https://trinitycore.info/en/database/master/world/creature_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'creature_template'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/creature_template_difficulty" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'creature_template_difficulty'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment |
| --- | --- | --- | :---: | :---: | --- | --- | --- |
| [entry](#entry) | int | unsigned | PRI | NO | 0 |  |  |
| [PathId](#pathid) | int | unsigned |  | NO | 0 |  |  |
| [mount](#mount) | int | unsigned |  | NO | 0 |  |  |
| [MountCreatureID](#mountcreatureid) | int | unsigned |  | NO | 0 |  |  |
| [StandState](#standstate) | tinyint | unsigned |  | NO | 0 |  |  |
| [AnimTier](#animtier) | tinyint | unsigned |  | NO | 0 |  |  |
| [VisFlags](#visflags) | tinyint | unsigned |  | NO | 0 |  |  |
| [SheathState](#sheathstate) | tinyint | unsigned |  | NO | 1 |  |  |
| [PvPFlags](#pvpflags) | tinyint | unsigned |  | NO | 0 |  |  |
| [emote](#emote) | int | unsigned |  | NO | 0 |  |  |
| [aiAnimKit](#aianimkit) | smallint | signed |  | NO | 0 |  |  |
| [movementAnimKit](#movementanimkit) | smallint | signed |  | NO | 0 |  |  |
| [meleeAnimKit](#meleeanimkit) | smallint | signed |  | NO | 0 |  |  |
| [visibilityDistanceType](#visibilitydistancetype) | tinyint | unsigned |  | NO | 0 |  |  |
| [auras](#auras) | mediumtext |  |  | YES | NULL |  |  |
&nbsp;
## Description of fields

### entry
This field signifies the creature_template.entry. It will affect all spawned creatures using that template entry.
&nbsp;

### PathId
If a creature has waypoint pathed movement, this field hold the [waypoint_path.PathId](/en/database/master/world/waypoint_path#PathId) for the path the creature is to follow.
&nbsp;

### mount
The model ID of the mount to be used to make the creature appear mounted. The value here overrides the value for the creature's unit field UNIT_FIELD_MOUNTDISPLAYID.
&nbsp;

### MountCreatureID
The [creature entry](../world/creature_template#entry) this creature is mounted on.
{.is-info}

&nbsp;

### StandState
| Name | Value |
| :--- | ---: |
| UNIT_STAND_STATE_STAND | 0 |
| UNIT_STAND_STATE_SIT | 1 |
| UNIT_STAND_STATE_SIT_CHAIR | 2 |
| UNIT_STAND_STATE_SLEEP | 3 |
| UNIT_STAND_STATE_SIT_LOW_CHAIR | 4 |
| UNIT_STAND_STATE_SIT_MEDIUM_CHAIR | 5 |
| UNIT_STAND_STATE_SIT_HIGH_CHAIR | 6 |
| UNIT_STAND_STATE_DEAD | 7 |
| UNIT_STAND_STATE_KNEEL | 8 |
| UNIT_STAND_STATE_SUBMERGED | 9 |
<br>

### AnimTier
| Name | Value | Description |
| :--- | ---: | --- |
| Ground | 0 | Plays ground tier animations |
| Swim | 1 | Falls back to ground tier animations, not handled by the client<br>Should never appear in sniffs, will prevent tier change animations from playing correctly if used |
| Hover | 2 | Plays flying tier animations or falls back to ground tier animations<br>Automatically enables hover clientside when entering visibility with this value |
| Fly | 3 | Plays flying tier animations |
| Submerged | 4 | |
<br>

### VisFlags
| Name | Value |
| :--- | ---: |
| UNIT_VIS_FLAGS_INVISIBLE     | 0x01 |
| UNIT_VIS_FLAGS_STEALTHED     | 0x02 |
| UNIT_VIS_FLAGS_UNTRACKABLE   | 0x04 |
| UNIT_VIS_FLAGS_UNK4          | 0x08 |
| UNIT_VIS_FLAGS_UNK5          | 0x10 |
<br>

### SheathState
> Creatures always have melee weapon ready if any unless specified otherwise.
{.is-info}

| Name | Value | Description |
| :--- | ---: | --- |
| SHEATH_STATE_UNARMED | 0 | Non prepared weapon    |
| SHEATH_STATE_MELEE   | 1 | Prepared melee weapon  |
| SHEATH_STATE_RANGED  | 2 | Prepared ranged weapon |
<br>

### PvPFlags
| Name | Value |
| :--- | ---: |
| UNIT_BYTE2_FLAG_NONE      | 0x00 |
| UNIT_BYTE2_FLAG_PVP       | 0x01 |
| UNIT_BYTE2_FLAG_UNK1      | 0x02 |
| UNIT_BYTE2_FLAG_FFA_PVP   | 0x04 |
| UNIT_BYTE2_FLAG_SANCTUARY | 0x08 |
| UNIT_BYTE2_FLAG_UNK4      | 0x10 |
| UNIT_BYTE2_FLAG_UNK5      | 0x20 |
| UNIT_BYTE2_FLAG_UNK6      | 0x40 |
| UNIT_BYTE2_FLAG_UNK7      | 0x80 |
<br>

### emote
Emote ID that the creature should continually perform.

A full list of emotes can be found at [wago.tools](https://wago.tools/db2/emotes){target=blank}
&nbsp;

### aiAnimKit
AnimKit ID from AnimKit.db2 that is applied on creature when spawned.
&nbsp;

### movementAnimKit
AnimKit ID from AnimKit.db2 that is applied on creature when spawned.
&nbsp;

### meleeAnimKit
AnimKit ID from AnimKit.db2 that is applied on creature when spawned.
&nbsp;

### visibilityDistanceType
This field controls the visibility distance for creatures:

Normal = 0,  100.0f  // default visible distance, 100 yards on continents

Tiny = 1,  25.0f

Small = 2,  50.0f

Large = 3, 200.0f

Gigantic = 4, 400.0f

Infinite = 5, SIZE_OF_GRIDS // max distance for visible objects
&nbsp;

### auras
This field controls any auras to be applied on the creature (both in effect and visually). To apply multiple auras, you can add more aura entries, separating each entry by a space. Remember that if a spell applies multiple auras.

List of useful aura entries (examples):

- '16380' - Makes the creature invisible.
- '18950' - Makes the creature detect other invisible units (players or creatures).
- '16380 18950' - Both auras above
&nbsp;

<a href="https://trinitycore.info/en/database/master/world/creature_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'creature_template'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/creature_template_difficulty" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'creature_template_difficulty'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
