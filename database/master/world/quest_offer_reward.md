---
title: quest_offer_reward
description:
published: true
date: 2022-12-19T18:40:58.945Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:35:10.470Z
---

<a href="https://trinitycore.info/en/database/master/world/quest_objectives_locale" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'quest_objectives_locale'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/quest_offer_reward_conditional" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'quest_offer_reward_conditional'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment |
| --- | --- | --- | :---: | :---: | --- | --- | --- |
| [ID](#id-alt) | int | unsigned | PRI | NO | 0 |  |  |
| [Emote1](#emote1) | smallint | signed |  | NO | 0 |  |  |
| [Emote2](#emote2) | smallint | signed |  | NO | 0 |  |  |
| [Emote3](#emote3) | smallint | signed |  | NO | 0 |  |  |
| [Emote4](#emote4) | smallint | signed |  | NO | 0 |  |  |
| [EmoteDelay1](#emotedelay1) | int | unsigned |  | NO | 0 |  |  |
| [EmoteDelay2](#emotedelay2) | int | unsigned |  | NO | 0 |  |  |
| [EmoteDelay3](#emotedelay3) | int | unsigned |  | NO | 0 |  |  |
| [EmoteDelay4](#emotedelay4) | int | unsigned |  | NO | 0 |  |  |
| [RewardText](#rewardtext) | mediumtext |  |  | YES | NULL |  |  |
| [VerifiedBuild](#verifiedbuild) | int | signed |  | NO | 0 |  |  |
&nbsp;
## Description of fields

### ID <!-- {#id-alt} -->
references [quest_template.ID](../world/quest_template#id)
&nbsp;

### Emote\[1-4]
[Emote ID](https://wago.tools/db2/emotes) played by NPC.
&nbsp;

### EmoteDelay\[1-4]
Emote delay in milliseconds.
&nbsp;

### RewardText
Quest gossip text shown when turning in a quest where no item delivery is involved.
&nbsp;

### VerifiedBuild
This field is used by the TrinityDB Team to determine whether a template has been verified from WDB files.

If value is 0 then it has not been parsed yet.

If value is above 0 then it has been parsed with WDB files from that specific client build.

If value is -1 then it is just a place holder until proper data are found on WDBs.

If value is -Client Build then it was parsed with WDB files from that specific client build and manually edited later for some special necessity.

&nbsp;

<a href="https://trinitycore.info/en/database/master/world/quest_objectives_locale" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'quest_objectives_locale'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/quest_offer_reward_conditional" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'quest_offer_reward_conditional'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
