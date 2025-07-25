---
title: skill_extra_item_template
description:
published: true
date: 2022-11-21T21:08:45.230Z
tags: database, master, world
editor: markdown
dateCreated: 2021-08-30T09:36:19.402Z
---

<a href="https://trinitycore.info/en/database/master/world/skill_discovery_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'skill_discovery_template'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/skill_fishing_base_level" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'skill_fishing_base_level'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>

## Structure

| Field | Type | Attributes | Key | Null | Default | Extra | Comment |
| --- | --- | --- | :---: | :---: | --- | --- | --- |
| [spellId](#spellid) | int | unsigned | PRI | NO | 0 |  | SpellId of the item creation spell |
| [requiredSpecialization](#requiredspecialization) | int | unsigned |  | NO | 0 |  | Specialization spell id |
| [additionalCreateChance](#additionalcreatechance) | float |  |  | NO | 0 |  | chance to create add |
| [additionalMaxNum](#additionalmaxnum) | tinyint | unsigned |  | NO | 0 |  | max num of adds |
&nbsp;
## Description of fields

### spellId
The [Spell ID](https://wago.tools/db2/spell) that creates the item.
&nbsp;

### requiredSpecialization
The character must have the [Spell ID](https://wago.tools/db2/spell) specified here learned to have a chance at triggering the extra item proc.
&nbsp;

### additionalCreateChance
The chance that the player will create an additional item.
&nbsp;

### additionalMaxNum
The number of extra copies that can be created.
**additionalCreateChance** is rolled for each attempt, until failure or reaching **additionalMaxNum**.
&nbsp;

#### Example
given **additionalCreateChance** = 35 and **additionalMaxNum** = 4:
| items created | chance of occurrence |
|------------|----------------------|
| 1 | 51.25% |
| 2 | 35.00% |
| 3 | 12.25% |
| 4 | 1.50% |
| 5 | 0.00% |
{.dense}


&nbsp;

<a href="https://trinitycore.info/en/database/master/world/skill_discovery_template" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-arrow-left theme--light"></i><span>Back to 'skill_discovery_template'</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/home" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><i aria-hidden="true" class="v-icon notranslate v-icon--left mdi mdi-home-outline theme--light"></i><span>Return to world</span></span></a>&nbsp;&nbsp;&nbsp;<a href="https://trinitycore.info/en/database/master/world/skill_fishing_base_level" class="mt-5 v-btn v-btn--depressed v-btn--flat v-btn--outlined theme--light v-size--default darkblue--text text--lighten-3"><span class="v-btn__content"><span>Go to 'skill_fishing_base_level'</span><i aria-hidden="true" class="v-icon notranslate v-icon--right mdi mdi-arrow-right theme--light"></i></span></a>
