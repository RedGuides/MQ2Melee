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
### {{ renderMember(type='bool', name='AggroMode') }}

:   TRUE/FALSE if the plugin is operating in Aggro-mode or not.

### {{ renderMember(type='int', name='Ammunition') }}

:   Count of defined ammunition or current equipped ammunition.

### {{ renderMember(type='float', name='BackAngle') }}

:   Angle representing heading difference with current target's back.

### {{ renderMember(type='bool', name='BackStabbing') }}

:   TRUE/FALSE if backstab setting is on/off.

### {{ renderMember(type='int', name='Casted') }}

:   Time (in miliseconds) elapsed since last detected spell casting (60000 if none).

### {{ renderMember(type='bool', name='Combat') }}

:   TRUE/FALSE if plugin enable and got valid kill target. Should replace ${Me.Combat} logic.

### {{ renderMember(type='int', name='DiscID') }}

:   Spell ID of currently running discipline, 0 if none.

### {{ renderMember(type='bool', name='Enable') }}

:   TRUE/FALSE if plugin on/off, NULL if not loaded.

### {{ renderMember(type='bool', name='Enrage') }}

:   True if enraged

### {{ renderMember(type='bool', name='GotAggro') }}

:   TRUE/FALSE if current target seems to be aggroed on you (not perfect).

### {{ renderMember(type='bool', name='Immobilize') }}

:   TRUE if you have been standing still for more then 250ms, FALSE if not.

### {{ renderMember(type='bool', name='Infuriate') }}

:   TRUE if kill target is infuriated!

### {{ renderMember(type='bool', name='MeleeMode') }}

:   TRUE/FALSE if melee mode is on/off.

### {{ renderMember(type='bool', name='RangeMode') }}

:   TRUE/FALSE if range mode is enabled (i.e. the `range` setting is > 0).

### {{ renderMember(type='string', name='Status') }}

:   Current plugin status, can be one or more of the following: ENGAGED, WAITING, MELEE, RANGE, ENRAGE, INFURIATE, BACKING, ESCAPING, FEIGNING, EVADING, FALLING, STEALING, BEGGING.

### {{ renderMember(type='int', name='Target') }}

:   SpawnID of current valid kill target, otherwise 0.

### {{ renderMember(type='float', name='ViewAngle') }}

:   Angle of view with current target.

### {{ renderMember(type='int', name='Hidden') }}

:   How long you've been hidden

### {{ renderMember(type='int', name='Silent') }}

:   How long you've been sneaking

### {{ renderMember(type='int', name='NumHits') }}

:   Total number of hits

### {{ renderMember(type='bool', name='XTaggro') }}

:   Returns TRUE if you are the highest on aggro for all mobs on your extended target window hate list. FALSE if another person has higher aggro on at least one of them.

<!--dt-members-end-->

<!--dt-linkrefs-start-->
[bool]: ../macroquest/reference/data-types/datatype-bool.md
[float]: ../macroquest/reference/data-types/datatype-float.md
[int]: ../macroquest/reference/data-types/datatype-int.md
[string]: ../macroquest/reference/data-types/datatype-string.md
<!--dt-linkrefs-end-->
