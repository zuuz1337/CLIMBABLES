---
title: ClickParts
parent: Object Tags
tags: [trigger, basepart, platforming]
---

# ClickPart
{: .no_toc }

ClickParts can be set to ON and OFF by clicking!

## On this page
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Attributes

| AttributeName | Value | Default |
|---------------|-------|---------|
| [OnCollision](#oncollision) | `bool` | `false` |
| [OnTransparency](#ontransparency) | `number` | `0.5` |
| [OnColor](#oncolor) | `Color3` | `part.Color` |
| [OffCollision](#offcollision) | `bool` | `false` |
| [OffTransparency](#offtransparency) | `number` | `0.5` |
| [OffColor](#offcolor) | `Color3` | `part.Color` |
| [SwitchMode](#switchmode) | `bool` | `false` |
| [Time](#time) | `number` | `1` |


> Inherits all attributes from [`setupTriggers`]({% link UtilityModules/behaviorutil.md %}#setuptriggers) when a TriggerConfiguration is present: `OneTimeUse`, `Cooldown`, and `Enabled`.

---

## Sounds

| SoundName | Condition |
|----------|---------|
| OnSound | Plays when set to ON. |
| OffSound | Plays when set to OFF. |

---

# Attributes

---

## OnCollision
Collision in the ON state

---

## OnTransparency
Transparency in the ON state

---

## CheckpointTrigger
Will trigger the spawn position change once turned to true, then it will be set to false again. (This attribute is created in-studio)


