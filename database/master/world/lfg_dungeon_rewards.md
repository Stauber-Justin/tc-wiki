---
title: lfg_dungeon_rewards
description:
published: true
date: 2022-11-21T21:06:10.218Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:32:47.895Z
---

<a href="https://trinitycore.info/en/database/master/world/jump_charge_params" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'jump_charge_params'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/lfg_dungeon_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'lfg_dungeon_template'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment |
| --- | --- | --- | :---: | :---: | --- | --- | --- |
| [dungeonId](#dungeonid) | int | unsigned | PRI | NO | 0 |  | Dungeon entry from dbc |
| [maxLevel](#maxlevel) | tinyint | unsigned | PRI | NO | 0 |  | Max level at which this reward is rewarded |
| [firstQuestId](#firstquestid) | int | unsigned |  | NO | 0 |  | Quest id with rewards for first dungeon this day |
| [otherQuestId](#otherquestid) | int | unsigned |  | NO | 0 |  | Quest id with rewards for Nth dungeon this day |
&nbsp;
## Description of fields

### dungeonId
references [LfgDungeons ID](https://wago.tools/db2/lfgdungeons)
&nbsp;

### maxLevel
Max level at which this reward is rewarded.
&nbsp;

### firstQuestId
[quest_template.ID](../world/quest_template#id) with rewards for the first dungeon this day.
&nbsp;

### otherQuestId
[quest_template.ID](../world/quest_template#id) with rewards for subsequent dungeons this day.
&nbsp;

<a href="https://trinitycore.info/en/database/master/world/jump_charge_params" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'jump_charge_params'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/lfg_dungeon_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'lfg_dungeon_template'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
