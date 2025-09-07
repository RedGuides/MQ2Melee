---
tags:
  - plugin
resource_link: "https://www.redguides.com/community/resources/mq2melee.287/"
support_link: "https://www.redguides.com/community/threads/mq2melee.23017/"
repository: "https://github.com/RedGuides/MQ2Melee"
config: "<server>_<character>.ini, MQ2Melee.ini(optional)"
authors: "s0rcier, Wasted, Jobey, htw, pms, Maskoi, teichou, cr4zyb4rd, rswiders, Nayenia, winnower, Saar, eqmule, alynel, Sic, ctaylor22, Redbot, Knightly, BigDorf"
tagline: "Automate melee skills & movement"
quick_start: "https://www.redguides.com/community/threads/mq2melee-examples-timers-and-multiline-and-healing-oh-my.71865/"
---

# MQ2Melee

<!--desc-start-->
MQ2Melee is used for assisting with melee skills, abilities, AA's and movement in combat. It can also be configured to handle pets and items depending on combat conditions.
<!--desc-end-->

## Commands

<a href="cmd-enrageoff/">
{% 
  include-markdown "projects/mq2melee/cmd-enrageoff.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-enrageoff.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-enrageoff.md') }}

<a href="cmd-enrageon/">
{% 
  include-markdown "projects/mq2melee/cmd-enrageon.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-enrageon.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-enrageon.md') }}

<a href="cmd-infuriateoff/">
{% 
  include-markdown "projects/mq2melee/cmd-infuriateoff.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-infuriateoff.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-infuriateoff.md') }}

<a href="cmd-infuriateon/">
{% 
  include-markdown "projects/mq2melee/cmd-infuriateon.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-infuriateon.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-infuriateon.md') }}

<a href="cmd-killthis/">
{% 
  include-markdown "projects/mq2melee/cmd-killthis.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-killthis.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-killthis.md') }}

<a href="cmd-melee/">
{% 
  include-markdown "projects/mq2melee/cmd-melee.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-melee.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-melee.md') }}

<a href="cmd-throwit/">
{% 
  include-markdown "projects/mq2melee/cmd-throwit.md" 
  start="<!--cmd-syntax-start-->" 
  end="<!--cmd-syntax-end-->" 
%}
</a>
:    {% include-markdown "projects/mq2melee/cmd-throwit.md" 
        start="<!--cmd-desc-start-->" 
        end="<!--cmd-desc-end-->" 
        trailing-newlines=false 
     %} {{ readMore('projects/mq2melee/cmd-throwit.md') }}

## Settings

To view the available settings for your character, type `/melee` in-game. Only the options relevant to your class will be shown. 
You can also refer to the [/melee](cmd-melee.md) page for more details. Most options in the INI file should be set using the 
command line `/melee command=on|off` rather than editing the INI file directly. 
When you set options this way, they are saved to the INI file when you use `/melee save`. 
Options that contain macro commands must be edited directly in the INI file and then loaded with `/melee load`.

Example TLP rogue INI from `server_charname.ini`

```ini
[MQ2Melee]
assassinate=0
backstab=1
disarm=0
enrage=0
escape=20
evade=0
facing=0
infuriate=1
melee=1
pickpocket=0
plugin=1
pothealover=25
resume=75
stickbreak=1
stickmode=1
stickrange=75
stickcmd=snaproll rear fast
```

### Conditional "IF" options

The following conditionals can be set in the INI file. They will then be evaluated before the relevant disc/skill is triggered.

!!! warning "Requirements"

    All conditions must take the form of `${If[condition,1,0]}` statements. For example: `withstandif=${If[${Melee.GotAggro},1,0]}` or slightly more complex, `withstandif=${If[${Melee.GotAggro} && ${Me.PctHPs}<80,1,0]}`.
    Your defined condition must not exceed 255 characters, or it will cause the plugin to crash.

<div class="grid cards" markdown>
- assaultif
- backstabif
- bashif
- beggingif
- aspif
- bviviif
- cloudif
- boastfulif
- bleedif
- bloodlustif
- callchallengeif
- cstrikeif
- crippleif
- gutpunchif
- opstrikeif
- throatjabif
- battleleapif
- challengeforif
- commandingif
- cryhavocif
- defenseif
- disarmif
- downshitif
- dragonpunchif
- eaglestrikeif
- enragingkickif
- eyegougeif
- evadeif
- fallsif
- feralswipeif
- fieldarmif
- fistofwuif
- fclaw
- flyingkickif
- forageif
- frenzyif
- gbladeif
- gorillasmashif
- harmtouchif
- holyshitif
- pothealfastif
- pothealoverif
- hideif
- intimidationif
- joltif
- jltkicksif
- jugularif
- kickif
- kneestrikeif
- knifeplayif
- layhandif
- leopardclawif
- mendif
- monkeyif
- opfrenzyif
- pickpocketif
- pinpointif
- provokeif
- ragevolleyif
- rakeif
- rallosif
- ravensif
- rightindif
- roundkickif
- sensetrapif
- selosif
- slamif
- slapfaceif
- sneakif
- steelyif
- stormbladesif
- strikeif
- stunningif
- synergyif
- tauntif
- thiefeyeif
- throwstoneif
- tigerclawif
- twistedshankif
- vigaxeif
- vigdaggerif
- vigshurikenif
- withstandif
- yaulp (no "if" on this one)
</div>

### Command Parameters

**`stickcmd=`**
:   This takes a list of options that should be passed to the [/stick](../mq2moveutils/cmd-stick.md) command.  
    Example: `stickcmd=hold 15`

**`strikecmd=`**
:   This takes a list of options that should be passed to the /stick command for rogue strike/assassination (must set `strikemode=1`).
    Example: `strikecmd=hold 15`

### HolyShit and DownShit

Yes, these are the real names. `HolyShit` is for combat, and `DownShit` is for out of combat.

!!! warning "Use with caution"
    When setting these in your `.ini`, you must be careful not to create an endless loop that will spam the game server. For your account's safety, make sure that when your line finishes it will set up something that will force it to be `FALSE` for a while!

<div class="grid cards" markdown>

-   __DownShit__ (Out of combat)

    ---
    These settings control actions performed when you are not in combat.

    - **`downshit0-90=`**
      Takes a macro command that will be run when you are <span class="accent">not in combat</span> and your cursor is free.

    - **`downflag0-90=`**
      Turn on/off the `downshit` with the same number.
        - `0`: Off
        - `1`: On (always parsed)
        - `2`: On, but only parsed if a macro is running. (use this for script variables)
        - `3`: On, but only parsed if no macro is running.

    !!! abstract "Enabling a `downshit`"
        You have to enable each option with `/melee downflag#=on`.

-   __HolyShit__ (In combat)

    ---
    These settings control actions performed during combat.

    - **`holyshit0-90=`**
      Takes a macro command that will be run <span class="accent">in combat</span> and your cursor is free.

    - **`holyflag0-90=`**
      Turn on/off the `holyshit` with the same number.
        - `0`: Off
        - `1`: On (always parsed)
        - `2`: On, but only parsed if a macro is running. (use this for script variables)
        - `3`: On, but only parsed if no macro is running.

    !!! abstract "Enabling a `holyshit`"
        You have to enable each option with `/melee holyflag#=on`.

</div>

### INI examples

```ini
; Will just echo that the macro is paused (this is stupid btw, but its an example.)
; SINCE WE USE A MACRO VARIABLE (ModVersion) WE NEED TO SET THE FLAG TO 2!
downflag0=2
downshit0=/if (${Macro.Paused}) /echo ${Macro} ${ModVersion} is PAUSED!
```

```ini
; Swapping an Avatar-proccing weapon when needed.
; - The first line swaps your Ancient Prismatic Spear [id=29435] into your offhand if you don't already have it equipped and you don't have the Avatar buff
; - The second line swaps your Orcish Bone Axe [id=82634] back into your offhand if it's not equipped and you have the Avatar buff already
holyshit0=/if (${Me.Inventory[offhand].ID}==82634 && !${Me.Buff[avatar].ID} && ${Spell[avatar].Stacks} && (${Melee.AggroMode} && ${Melee.GotAggro})) /exchange 29435 offhand
holyshit1=/if (${Me.Inventory[offhand].ID}==29435 && (${Me.Buff[avatar].ID} || !${Spell[avatar].Stacks} || (${Melee.AggroMode} && !${Melee.GotAggro}))) /exchange 82634 offhand
```

```ini
; Activating the Area Taunt AA when multiple mobs in range
holyshit2=/if (${Melee.Combat} && ${SpawnCount[npc radius 50 zradius 10]}>1 && ${Me.AltAbilityReady[area taunt]} && ${Melee.AggroMode}) /alt activate 110
```

```ini
; Forage if you have a chest item (usually used to check if you awaiting a rez) and your cursor is free
forageif=${If[${Me.Inventory[chest].ID} && !${Cursor.ID},1,0]}
```

```ini
;Swap in and click monk epic haste gloves [id=10652] (or monk ornate gloves [id=12623]) if needed
holyshit0=/if (!${Me.Buff[Celestial Tranquility].ID} && ${Spell[Celestial Tranquility].Stacks} && ${Me.FreeBuffSlots}>=1) /casting 10652|hands
```

```ini
;For monks, toggle enrage detection if you have Master's Aura (makes you immune to enrage)
holyshit2=/if (!${Me.Song[Master's Aura Effect].ID} && !${meleemvi[enrage]}) /melee enrage=1
holyshit3=/if (${Me.Song[Master's Aura Effect].ID} && ${meleemvi[enrage]}) /melee enrage=0
```

```ini
; During downtime, check my clicky buffs and recast them if needed
downshit0=/if (${Spell[Form of Defense I].Stacks} && !${Me.Buff[Form of Defense I].ID} && !${Me.Moving}) /casting "Shroud of the Fallen Defender"|back
downshit1=/if (${Spell[Shield of the Arcane].Stacks} && !${Me.Buff[Shield of the Arcane].ID} && !${Me.Moving}) /casting "Kizrak's Chestplate of Battle"|chest
```

```ini
; Cast my clicky DS ring during combat if needed (it's insta-cast, so I can do so while in combat without affecting anything)
holyshit4=/if (${Spell[Shield of the Eighth].Stacks} && !${Me.Buff[Shield of the Eighth].ID}) /casting "Velium Coldain Insignia Ring"|item
```

```ini
;Uses crippling strike to snare
holyshit4=/if (${Target.CurrentHPs}<20 && ${Target.Speed}>50) /disc crippling strike
```

```ini
;During downtime, check my aura's and recast if needed
downshit1=/if (!${Spell[${Me.Aura[1]}].ID} && !${Me.Moving} && !${Me.Invis} && ${Me.PctEndurance} > 4 && ${Me.Standing}) /disc Myrmidon's Aura
```

```ini
;Activate Respite on Warrior if Endurance is low and deactivate running defensive if needed
downshit1=/if (${Me.PctEndurance}<25 && ${Me.CombatAbilityReady[Respite Rk. II]} && ${Me.CurrentEndurance}>100 && (${Zone.ID}!=344)) /disc Respite Rk. II
downshit2=/if (${Window[CombatAbilityWnd].Child[CAW_CombatEffectLabel].Text.Equal[Staunch Defense Rk. II]} && ${Me.PctEndurance}<25) /notify CombatAbilityWnd CAW_CombatEffectButton leftmouseup
```

```ini
;Change cleric merc to reactive on named mobs, to balanced on non named mobs. Easily adjustable for DPS mercs
holyshit1=/if (!${Target.Named} && ${Mercenary.State.Equal[ACTIVE]} && ${Mercenary.Stance.NotEqual[Balanced]} && ${Mercenary.Class.Name.Equal[Cleric]}) /stance balanced
holyshit2=/if (${Target.Named} && ${Mercenary.State.Equal[ACTIVE]} && ${Mercenary.Stance.NotEqual[Reactive]} && ${Mercenary.Class.Name.Equal[Cleric]}) /stance reactive
```

```ini
;Pal/Sk check if target is undead and is not otherwise slowed, then use Helix of the Undying
holyshit4=/if (${Target.Body.Name.Equal[Undead]} && ${Me.AltAbilityReady[2018]} && !${Bool[${Target.Slowed}]}) /alt activate 2018
;Alernatively a slow weapon exchange using the Bandolier and mainhand check, if there is no enc/sham nearby to slow
holyshit19=/if (!${Bool[${Target.Slowed}]} && ${Me.Inventory[mainhand].ID}!=133167  && !${SpawnCount[pc class shaman radius 50]} && !${SpawnCount[pc class enchanter radius 50]}) /Bandolier Activate Slow
holyshit20=/if (${Bool[${Target.Slowed}]} && ${Me.Inventory[mainhand].ID}!=140616) /Bandolier Activate 1Hand
```

```ini
;Necro - utilize the aggro meter to FD off aggro when over a set percentage
holyshit3=/if (${Me.PctAggro}>80 && ${Target.Distance}<15) /casting "Improved Death Peace" alt
```

```ini
;Sk centric but can be edited for use with any tank
;first line checks if first damage mod disc is ready, the target is named , endurance is over needed amount, and there is no current disc running
;second line does the same as first, but also check that first damage mod disc is unavailable
;third line does same as second , except it also checks that the second damage mod disc is unavailable
holyshit7=/if (${Me.CombatAbilityReady[${Spell[Unholy Guardian Discipline].RankName}]} && ${Target.Named} && ${Me.CurrentEndurance}>5300 && !${Melee.DiscID}) /disc ${Spell[Unholy Guardian Discipline].RankName}
holyshit8=/if (${Me.CombatAbilityReady[${Spell[Doomscale Mantle].RankName}]} && !${Me.CombatAbilityReady[${Spell[Unholy Guardian Discipline].RankName}]} && ${Target.Named} && ${Me.CurrentEndurance}>7700 && !${Melee.DiscID}) /disc ${Spell[Doomscale Mantle].RankName}
holyshit9=/if (${Me.CombatAbilityReady[${Spell[Grelleth's Carapace].RankName}]} && !${Me.CombatAbilityReady[${Spell[Doomscale Mantle].RankName}]} && !${Me.CombatAbilityReady[${Spell[Unholy Guardian Discipline].RankName}]} && ${Target.Named} && ${Me.CurrentEndurance}>2700 && !${Melee.DiscID}) /disc ${Spell[Grelleth's Carapace].RankName}
```

More examples can be found in the [support thread](https://www.redguides.com/community/threads/mq2melee.23017/).

### Optional Global INI File

MQ2Melee has 3 global parameters that can be set in an optional INI file, which must be manually created. MQ2Melee uses default values for these parameters unless it finds a file named MQ2Melee.ini that you created in the same directory. Here's an example of a `MQ2Melee.ini`:

```ini
[Settings]
SpawnType=10
;0 + all desired target type modifier: (+1 PC) (+2 NPC) (+4 PC PET) (+8 NPC PET) (+16 PC CORPSE) (+32 NPC CORPSE) default is 10 (0 for base + 2 for NPC and + 8 for NPC PET).
MeleeKeys=z
;Melee Attack Key (not same as eq please unless you like problems) default is z.
RangeKeys=x
;Range Attack Key default is x.
Bindings=1
;Set key bindings? (1 for yes, 0 for no) default is 1.
```

## Top-Level Objects

## [Melee](tlo-melee.md)
{% include-markdown "projects/mq2melee/tlo-melee.md" start="<!--tlo-desc-start-->" end="<!--tlo-desc-end-->" trailing-newlines=false %} {{ readMore('projects/mq2melee/tlo-melee.md') }}

## [meleemvb](tlo-meleemvb.md)
{% include-markdown "projects/mq2melee/tlo-meleemvb.md" start="<!--tlo-desc-start-->" end="<!--tlo-desc-end-->" trailing-newlines=false %} {{ readMore('projects/mq2melee/tlo-meleemvb.md') }}


## [meleemvi](tlo-meleemvi.md)
{% include-markdown "projects/mq2melee/tlo-meleemvi.md" start="<!--tlo-desc-start-->" end="<!--tlo-desc-end-->" trailing-newlines=false %} {{ readMore('projects/mq2melee/tlo-meleemvi.md') }}

## [meleemvs](tlo-meleemvs.md)
{% include-markdown "projects/mq2melee/tlo-meleemvs.md" start="<!--tlo-desc-start-->" end="<!--tlo-desc-end-->" trailing-newlines=false %} {{ readMore('projects/mq2melee/tlo-meleemvs.md') }}

## DataTypes

## [Melee](datatype-melee.md)
{% include-markdown "projects/mq2melee/datatype-melee.md" start="<!--dt-desc-start-->" end="<!--dt-desc-end-->" trailing-newlines=false %} {{ readMore('projects/mq2melee/datatype-melee.md') }}

<h2>Members</h2>
{% include-markdown "projects/mq2melee/datatype-melee.md" start="<!--dt-members-start-->" end="<!--dt-members-end-->" %}
{% include-markdown "projects/mq2melee/datatype-melee.md" start="<!--dt-linkrefs-start-->" end="<!--dt-linkrefs-end-->" %}
