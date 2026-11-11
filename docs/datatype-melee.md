---
tags:
  - datatype
---
# `Melee`

<!--dt-desc-start-->
Contains members the report status of plugin variables and current target(s)
<!--dt-desc-end-->

## Members
<!--dt-members-start-->
/// member | bool AggroMode
TRUE/FALSE if the plugin is operating in Aggro-mode or not.
///

/// member | int Ammunition
Count of defined ammunition or current equipped ammunition.
///

/// member | float BackAngle
Angle representing heading difference with current target's back.
///

/// member | bool BackStabbing
TRUE/FALSE if backstab setting is on/off.
///

/// member | int Casted
Time (in miliseconds) elapsed since last detected spell casting (60000 if none).
///

/// member | bool Combat
TRUE/FALSE if plugin enable and got valid kill target. Should replace ${Me.Combat} logic.
///

/// member | int DiscID
Spell ID of currently running discipline, 0 if none.
///

/// member | bool Enable
TRUE/FALSE if plugin on/off, NULL if not loaded.
///

/// member | bool Enrage
True if enraged
///

/// member | bool GotAggro
TRUE/FALSE if current target seems to be aggroed on you (not perfect).
///

/// member | bool Immobilize
TRUE if you have been standing still for more then 250ms, FALSE if not.
///

/// member | bool Infuriate
TRUE if kill target is infuriated!
///

/// member | bool MeleeMode
TRUE/FALSE if melee mode is on/off.
///

/// member | bool RangeMode
TRUE/FALSE if range mode is enabled (i.e. the `range` setting is > 0).
///

/// member | string Status
Current plugin status, can be one or more of the following: ENGAGED, WAITING, MELEE, RANGE, ENRAGE, INFURIATE, BACKING, ESCAPING, FEIGNING, EVADING, FALLING, STEALING, BEGGING.
///

/// member | int Target
SpawnID of current valid kill target, otherwise 0.
///

/// member | float ViewAngle
Angle of view with current target.
///

/// member | int Hidden
How long you've been hidden
///

/// member | int Silent
How long you've been sneaking
///

/// member | int NumHits
Total number of hits
///

/// member | bool XTaggro
Returns TRUE if you are the highest on aggro for all mobs on your extended target window hate list. FALSE if another person has higher aggro on at least one of them.
///

<!--dt-members-end-->

<!--dt-linkrefs-start-->
[bool]: ../macroquest/reference/data-types/datatype-bool.md
[float]: ../macroquest/reference/data-types/datatype-float.md
[int]: ../macroquest/reference/data-types/datatype-int.md
[string]: ../macroquest/reference/data-types/datatype-string.md
<!--dt-linkrefs-end-->
