---
title: creature_model_info
description:
published: true
date: 2022-11-21T21:04:02.281Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:29:57.796Z
---

<a href="https://trinitycore.info/en/database/master/world/creature_loot_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'creature_loot_template'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/creature_movement_info" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'creature_movement_info'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment | Source in sniff |
| --- | --- | --- | :---: | :---: | --- | --- | --- | --- |
| [DisplayID](#displayid) | int | unsigned | PRI | NO | 0 |  |  | SMSG_UPDATE_OBJECT |
| [BoundingRadius](#boundingradius) | float |  |  | NO | 0 |  |  | SMSG_UPDATE_OBJECT |
| [CombatReach](#combatreach) | float |  |  | NO | 0 |  |  | SMSG_UPDATE_OBJECT |
| [DisplayID_Other_Gender](#displayid_other_gender) | int | unsigned |  | NO | 0 |  |  | manually |
| [VerifiedBuild](#verifiedbuild) | int | signed |  | NO | 0 |  |  | generated |
&nbsp;
## Description of fields

### DisplayID
DisplayID from [CreatureDisplayInfo.db2](https://wago.tools/db2/creaturedisplayinfo){target=_blank}
&nbsp;

### BoundingRadius
This field is unused. It's purpose is currently unknown. It may or may not be linked to path-finding.
&nbsp;

### CombatReach
This value is the unit's radius in term of game mechanics: The bigger this value is, the higher the unit's range is and also the further away it can get hit from.
&nbsp;

### DisplayID_Other_Gender
DisplayID for other gender from [CreatureDisplayInfo.db2](https://wago.tools/db2/creaturedisplayinfo){target=_blank}
&nbsp;

### VerifiedBuild
This field is used by the TrinityDB Team to determine whether a template has been verified from WDB files.

If value is 0 then it has not been parsed yet.

If value is above 0 then it has been parsed with WDB files from that specific client build.

If value is -1 then it is just a place holder until proper data are found on WDBs.

If value is -Client Build then it was parsed with WDB files from that specific client build and manually edited later for some special necessity.

&nbsp;

<a href="https://trinitycore.info/en/database/master/world/creature_loot_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'creature_loot_template'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/creature_movement_info" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'creature_movement_info'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
