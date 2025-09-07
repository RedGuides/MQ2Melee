---
tags:
  - command
---

# /melee

## Syntax

<!--cmd-syntax-start-->
```eqcommand
/melee [on|off] [setting=on|off]... [setting=<int>]...
```
<!--cmd-syntax-end-->

## Description

<!--cmd-desc-start-->
Turns settings on and off, sets items for settings that require them, and turns the plugin on and off. `/melee` by itself will list all settings that are available to your character.
<!--cmd-desc-end-->

## Options

<div class="rg-box-secondary" markdown>
This is a list of all available options for the `/melee` command. The options are grouped by class for readability.
</div>

=== "General"

    | Option | Description |
    |--------|-------------|
    | **(no option)** | List all settings that are available to your character. |
    | `on|off` | Turns the plugin on or off |
    | `save` | Saves settings to the configuration file |
    | `reload` | reload the configuration file. Helpful if you're editing the file directly. |
    | `debug=on|off` | Turns on debugging output for the plugin. |
    | `aggro=on|off` | Plugin tries to keep aggro on target using all enabled aggro abilities/disciplines until aggro is regained, or either you or the target dies. |
    | `aggropri=<itemID>` | Item ID for primary weapon to be used in aggro mode. |
    | `aggrosec=<itemID>` | Item ID for secondary weapon to be used in aggro mode. |
    | `arrow=<itemID>` | Item ID of ammunition to use for ranged/throwing attacks. |
    | `backoff=<0-100>` | Turns attack off if your life percentage goes below the designated value. Will never back off due to low health if aggro=on. |
    | `bash=on|off` | Will try to bash target if you have a shield equipped or have a 2-handed weapon and the appropriate Two-Handed Bash AA for your class. |
    | `battleleap=on|off` | Whether or not to use Battle Leap AA (Default=0/off) |
    | `bow=<itemID>` | Item ID for ranged weapon. |
    | `begging=on|off` | Will turn attack off and beg target and turn back on. |
    | `disarm=on|off` | Will try to disarm target if target is wielding a weapon. |
    | `downflag<0-90>=on|off` | Whether or not to use defined `DownShit<0-90>` from ini. e.g. `downflag0=on`<br>`on` or `1`: always on.<br>`off` or `0`: always off.<br>`2`: on only when a macro is running.<br>`3`: on only when no macro is running.<br>After enabling this option for the first time, you must edit the INI file with your relevant DownShit command and then issue /melee load to enable it. |
    | `enrage=on|off` | Turns attack off and issues /pet hold (/pet back if hold not available) if target enrages and you are facing it. Automatically re-engages when enrage ends or if you are behind the target. |
    | `facing=on|off` | Whether or not to face target (checked every 2 seconds and only in ranged mode). |
    | `feigndeath=<0-100>` | Attempt to feign death when life is below [X]%. 0=Off |
    | `holyflag<0-90>=on|off` | Whether or not to use defined HolyShit<0-90> from ini. e.g. `holyflag0=on`<br>`on` or `1`: always on.<br>`off` or `0`: always off.<br>`2`: on only when a macro is running.<br>`3`: on only when no macro is running.<br>After enabling this option for the first time, you must edit the INI file with your relevant HolyShit command and then issue /melee load to enable it. |
    | `infuriate=on|off` | Turns attack off and issues /pet hold (/pet back if hold not available) if target infuriates and you are facing it. Re-engages when infuriate ends or if you are behind the target. |
    | `intimidation=on|off` | Will use intimidation if available. |
    | `jolt=<#>` | Jolt every # of hits. This setting is used by Berserkers, Beastlords, and Rangers. See the class-specific tabs. |
    | `kick=on|off` | Will use kick if available. |
    | `melee=on|off` | Turn Melee Mode On/Off. |
    | `meleepri=<itemID>` | Item ID for primary weapon to be used in non-aggro mode. |
    | `meleesec=<itemID>` | Item ID for secondary weapon to be used in non-aggro mode |
    | `petassist=on|off` | Will send pet attack on engage and backoff on enrage/infuriate if those options are enabled. The plugin will also use /pet hold if you have that AA. |
    | `petdelay=<0-30>` | Will not engage pet until [x] seconds has passed. |
    | `petmend=<0-30>` | Cast "Mend Companion" or "Replenish Companion" if pet is at or below given health % (will cast higher of the two if you have both). |
    | `petrange=<0-150>` | Will not engage pet until mob is within [x] range of your pet. |
    | `pickpocket=on|off` | Turn off attack & try to pickpocket if not in aggro mode. |
    | `plugin=on|off` | Turn plugin on/off. |
    | `pothealfast=<0-100>` | Use fast heal potion when my HP falls below [X]% (default=30). |
    | `pothealover=<0-100>` | Use heal over time potion when my HP falls below [X]% (default=60). |
    | `provoke0=<ID>` | ID of the Disc/AA/Spell to use for provoking (0=off). |
    | `provoke1=<ID>` | ID of the Disc/AA/Spell to use for provoking (0=off) |
    | `provokeend=<0-100>` | Stop trying to provoke when target's health falls below [X]% (default=15). |
    | `provokemax=<0-100>` | Number of times you will try provoking aa/disc/spells to regain aggro (default=1). |
    | `provokeonce=on|off` | Only use provoke once to attempt to gain aggro. |
    | `range=<0-250>` | Enables ranged attacks when target is at or beyond this range. Note that 0 disables ranged attacks completely. |
    | `resume=<0-100>` | Stand up and turn back attack on if your life percentage goes above this value. Used with /melee feigndeath=on. |
    | `shield=<itemID>` | Item ID of shield to use for bashing |
    | `slam=on|off` | Will slam as often as possible. |
    | `sneak=on|off` | Will try to sneak if not in combat. |
    | `standup=on|off` | Will stand you on a failed FD. |
    | `stickdelay=<0-100>` | Wait [X] seconds before sticking to target. |
    | `stickmode=[0|1|2]` | If 1, it will use the stickcmd as defined in the INI file, if 0, it will use the default stick command, if 2, it will turn off sticking |
    | `stickrange=<#>` | Enables sticking when target is at set distance away (0=no sticking). |
    | `stun0=<ID>` | ID of the Disc/AA/Spell to use for stunning (0=off). |
    | `forage=on|off` | Turns forage on and off |
    | `petengagehps=<0-100>` | Pet engage when current target is below % |
    | `stickbreak=on|off` | on/1: stop stick on manual keyboard press<br>off/0: normal, no override |
    | `sticknorange=on|off` | off: normal  on: no range checks |
    | `hide=on|off` | Will try to hide if you're not in combat and not moving |
    | `stun1=<ID>` | ID of the Disc/AA/Spell to use for stunning (0=off). |
    | `stunning=<0-100>` | Cast defined Stun spell(s) if target at or below [X]% and/or if detected that target is casting a spell. |
    | `taunt=on|off` | Will push taunt button if aggro=on and you're not the target's target. Without a TauntIF statement, this will cause your toon to chain taunt. If you do not wish for that, use a TauntIF setting. |
    | `throwstone=<0-100>` | Will use throw stone disc when ready and target in range. Note: Will not use in aggro/provoke mode if provoke has not been used yet. |
    | `yaulp=on|off` | Yaulp on or off |

=== "Bard"

    | Option | Description |
    |--------|-------------|
    | `selos=on|off` | Selo's Kick |
    | `boastful=on|off` | Boastful Bellow |

=== "Beastlord"
    | Option | Description |
    |--------|-------------|
    | `asp=on|off` | Bite of the Asp |
    | `bvivi=<0-100>` | Use ability when endurance above [X]%. 0=Off<br>: Bestial Vivisection, Bestial Rending, Bestial Evulsing, etc. |
    | `cstrike=on|off` | Chameleon Strike |
    | `feralswipe=on|off` | Feral Swipe |
    | `fclaw=<0-100>` | Use ability when endurance above [X]%. 0=Off <br>: Flurry of Claws, Tumult of Claws, Clamor of Claws, etc. |
    | `gorillasmash=on|off` | Gorilla Smash |
    | `jolt=<#>` | Triggers every # of melee hits. <br>: Roar of Thunder |
    | `rake=<0-100>` | Use ability when endurance above [X]%. 0=Off <br>: Rake, Foray, Harrow, Rush, Barrage, Pummel, Maul, Mangle, Batter, Clobber |
    | `**ravens**=on|off` | Raven's Claw |

=== "Berserker"
    | Option | Description |
    |--------|-------------|
    | `bloodlust=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Shared Bloodlust, Shared Brutality, Shared Savagery, Shared Viciousness, Shared Cruelty, Shared Ruthlessness, Shared Atavism, Shared Violence |
    | `cripple=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Leg Strike, Leg Cut, Leg Slice, Crippling Strike, Tendon Cleave, Tendon Sever, Tendon Shear, Tendon Lacerate, Tendon Slash, Tendon Gash, Tendon Tear, Tendon Rupture, Tendon Rip, Tendon Shred |
    | `cryhavoc=<0-100>` | Cry Havoc. Use ability when endurance above [X]% (0=off). <br>: Cry Havoc, Cry Carnage |
    | `frenzy=on|off` | Frenzy on or off |
    | `jolt=<#>` | Triggers every # of melee hits. <br>: Diversive Strike, Distracting Strike, Confusing Strike, Baffling Strike, Jarring Strike, Jarring Smash, Jarring Clash, etc. |
    | `opfrenzy=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Overpowering Frenzy, Overwhelming Frenzy, Vanquishing Frenzy, Demolishing Frenzy, Mangling Frenzy, Vindicating Frenzy, Oppressing Frenzy |
    | `ragevolley=<0-100>` | Will use best ragevolley discipline that is available, ready and endurance above [X]% (0=off). <br>: Rage Volley, Destroyer's Volley, Giant Slayer's Volley, Annihilator's Volley, Decimator's Volley, Eradicator's Volley, Savage Volley, Sundering Volley, Brutal Volley, Demolishing Volley, Mangling Volley, Vindicating Volley, Pulverizing Volley |
    | `rallos=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Axe of Rallos, Axe of Graster, Axe of Illdaera, Axe of Zurel, Axe of Numicia, Axe of the Aeons, Axe of Empyr, Axe of Rekatok, Axe of Derakor, Axe of Xin Diabo |
    | `slapface=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Slap in the Face, Kick in the Teeth, Punch in the Throat, Kick in the Shins, Sucker Punch, Rabbit Punch, Swift Punch |
    | `vigaxe=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Vigorous Axe Throw, Energetic Axe Throw, Spirited Axe Throw, Brutal Axe Throw, Demolishing Axe Throw, Mangling Axe Throw, Vindicating Axe Throw, Maiming Axe Throw |

=== "Monk"
    | Option | Description |
    |--------|-------------|
    | `dragonpunch=on|off` | Dragon Punch, Tail Rake (Iksar) |
    | `falls=on|off` | Auto feign death |
    | `cloud=<0-100>` | Cloud of Fists, Phantom Partisan, Phantom Pummeling, Phantom Fisticuffs |
    | `fistsofwu=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Fists of Wu |
    | `leopardclaw=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Leopard Claw, Dragon Fang, Clawstriker Flurry, Wheel Of Fists, Whorl Of Fists, Six-Step Pattern, Seven-Step Pattern, Eight-Step Pattern, Torrent of Fists, Firestorm of Fists, Barrage of Fists, Buffeting of Fists |
    | `monkey=<0-100>` | Use ability when endurance above [X]% (0=off) <br>: Drunken Monkey Style |
    | `synergy=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Calanin's Synergy, Dreamwalker's Synergy, Veilwalker's Synergy, Shadewalker's Synergy, Doomwalker's Synergy, Firewalker's Synergy, Icewalker's Synergy, Bloodwalker's Synergy |
    | `vigshuriken=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Vigorous Shuriken |
    | `eaglestrike=on|off` | Eagle Strike |
    | `flyingkick=on|off` | Flying Kick |
    | `mend=<0-100>` | Mend wounds if your life percentage goes below the designated value. |
    | `roundkick=on|off` | Round Kick |
    | `tigerclaw=on|off` | Tiger Claw |

=== "Paladin"
    | Option | Description |
    |--------|-------------|
    | `layhand=<0-100>` | Lay Hands on myself when my HP % falls below [X]. |
    | `rightidg=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Righteous Indignation, Righteous Vexation, Righteous Umbrage, Righteous Condemnation, Righteous Antipathy, Righteous Censure |
    | `withstand=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Withstand, Defy, Renounce, Reprove, Repel, Spurn, Thwart, Repudiate |
    | `challengefor=on|off` | Activate aggro spells. <br>: Challenge for Honor, Trial for Honor, Charge for Honor, Confrontation for Honor, Provocation for Honor, Demand for Honor, Impose for Honor, Refute for Honor, Protest for Honor, Parlay for Honor |
    | `steely=on|off` | Activate defensive spells. <br>: Steely Stance, Stubborn Stance, Stoic Stance, Steadfast Stance, Staunch Stance, Defiant Stance, Stormwall Stance, Adamant Stance |

=== "Ranger"
    | Option | Description |
    |--------|-------------|
    | `enragingkick=<0-100>` | Enraging kick when life below % <br>: Enraging Crescent Kicks, Enraging Heel Kicks, Enraging Cut Kicks, etc. |
    | `jolt=<#>` | Triggers every # of melee hits. <br>: Jolt, Cinder Jolt |
    | `jltkicks=<0-100>` | endurance %<br>: Jolting Kicks, Jolting Snapkicks, Jolting Frontkicks, Jolting Hook Kicks, Jolting Crescent Kicks, Jolting Heel Kicks, Jolting Cut Kicks, Jolting Wheel Kicks, Jolting Axe Kicks, Jolting Roundhouse Kicks |
    | `stormblades=on|off` | Storm of Blades, Focused Storm of Blades, Squall of Blades, Focused Squall of Blades, Gale of Blades, Focused Gale of Blades, Blizzard of Blades, Tempest of Blades |

=== "Rogue"
    | Option | Description |
    |--------|-------------|
    | `assassinate=on|off` | Activate the assassinate skill (ie. Sneak, Hide, move behind target, activate Strike disc, backstab). |
    | `poker=<itemID>` | Item ID for backstabbing weapon. Will be swapped in before backstabbing if necessary. |
    | `sensetraps=on|off` | Will try to sense traps if not in combat |
    | `assault=<0-100>` | Use ability when endurance above [X]% (0=off). <br>Assault, Battery, Onslaught, Incursion, Barrage, Fellstrike, Blitzstrike, Shadowstrike |
    | `bleed=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Bleed, Wound, Lacerate, Gash, Hack, Slice, Slash, Lance |
    | `jugular=<0-100>` | Use ability when endurance above [X]% (0=off)<br>: Jugular Slash, Jugular Slice, Jugular Sever, Jugular Gash, Jugular Lacerate, Jugular Hack, Jugular Strike, Jugular Cut, Jugular Rend |
    | `pinpoint=<0-100>` | Use ability when endurance above [X]% (0=off) <br>: Pinpoint Vulnerability, Pinpoint Weaknesses, Pinpoint Vitals, Pinpoint Flaws, Pinpoint Liabilities, Pinpoint Deficiencies, Pinpoint Shortcomings, Pinpoint Defects |
    | `strike=on|off` | Use your best sneak attack disc <br>: Sneak Attack, Thief's Vengeance, Assassin Strike, Kyv Strike, Ancient Chaos Strike, Daggerfall, Razor Arc, Swiftblade, Daggerlunge, Daggerswipe, Daggerstrike, Daggerthrust, Daggergash, Daggerslice, Daggerslash |
    | `thiefeye=<0-100>` | Uses ability if your endurance is over [X]%. (0=off). <br>: Thief's Eye, Thief's Vision |
    | `vigdagger=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Vigorous Dagger-Throw, Vigorous Dagger-Strike, Energetic Dagger-Strike, Energetic Dagger-Throw, Exuberant Dagger-Throw, Forceful Dagger-Throw, Powerful Dagger-Throw, Precise Dagger-Throw |
    | `backstab=on|off` | Will try to back stab if you wielding a piercing weapon in your main hand and behind the target. |
    | `knifeplay=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Knifeplay |
    | `escape=<0-100>` | Turn off Attack and use rogue escape skill if your life percentage goes below the designated value. Will never happen if aggro=on. |
    | `twistedshank=on|off` | Twisted shank on or off |
    | `strikemode=on|off` | use strikecmd from ini? on = yes, off = no |
    | `evade=on|off` | Will attempt to evade in fight to drop some aggro each time hide skill available, strongly suggest that you set unhide=1 to authorize plugin to break invis and rejoin the fight. |
    | `pickpocket=on|off` | Turn off attack & try to pickpocket if not in aggro mode. |

=== "Shadow Knight"
    | Option | Description |
    |--------|-------------|
    | `harmtouch=on|off` | Use Harm Touch ability when ready. |
    | `gblade=<0-100>` | Use ability when endurance above [X]% (0=off). <br>:Gouging Blade, Gashing Blade, Lacerating Blade, Wounding Blade, Rending Blade, Grisly Blade |
    | `withstand=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Withstand, Defy, Renounce, Reprove, Repel, Spurn, Thwart, Repudiate |
    | `challengefor=on|off` | Activate aggro spells. <br>: Challenge for Power, Trial for Power, Charge for Power, Confrontation for Power, Provocation for Power, Demand for Power, Impose for Power, Refute for Power, Protest for Power, Parlay for Power |
    | `steely=on|off` | Activate defensive spells. <br>: Steely Stance, Stubborn Stance, Stoic Stance, Steadfast Stance, Staunch Stance, Defiant Stance, Stormwall Stance, Adamant Stance |

=== "Warrior"
    | Option | Description |
    |--------|-------------|
    | `callchallenge=on|off` | Call of Challenge |
    | `gutpunch=on|off` | Use Alt Ability when ready. Gut Punch |
    | `kneestrike=on|off` | Knee Strike. Use alt ability when ready |
    | `defense=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Bracing Defense, Staunch Defense, Stalwart Defense, Steadfast Defense, Stout Defense, Resolute Defense, Courageous Defense, Primal Defense |
    | `commanding=<0-100>` | Use ability when endurance above [X]% (0=off). Commanding Voice |
    | `fieldarm=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Field Armorer, Field Outfitter, Field Defender, Field Guardian, Field Protector, Field Champion, Paragon Champion, Full Moon's Champion |
    | `opportunisticstrike=<0-100>` | Use ability when endurance above [X]% (0=off). <br>: Opportunistic Strike, Strategic Strike, Vital Strike, Calculated Strike, Cunning Strike, Precision Strike, Exploitive Strike |
    | `throatjab=<0-100>` | Use ability when endurance above [X]% (0=off). |

## Examples

- All options listed with on/off as the arguments to enable/disable the option can use true or 1 in place of on, and false or 0 can be used in place of off.

```bash
/melee on aggro=on taunt=on kick=1 bash=0 intimidation=false disarm=true
```
