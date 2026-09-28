---
title: Checkpoint
parent: Object Tags
tags: [trigger, basepart, character]
---

# Checkpoint
{: .no_toc }

Checkpoints allow you to set a new spawn position on trigger, with an option to also set teams!

## On this page
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Attributes

| AttributeName | Value | Default |
|---------------|-------|---------|
| [ChangeToTeam](#changetoteam) | `string` | `""` |
| [TeamColor](#teamcolor) | `BrickColor` | `BrickColor.Random()` |
| [CheckpointTrigger](#checkpointTrigger) | `bool` | `false` |

> Inherits all attributes from [`setupTriggers`]({% link UtilityModules/behaviorutil.md %}#setuptriggers) when a TriggerConfiguration is present: `OneTimeUse`, `Cooldown`, and `Enabled`.

---

## Sounds

| SoundName | Condition |
|----------|---------|
| CheckpointReached | Plays on trigger. |

---

# Attributes

---

## ChangeToTeam
Will move the player to the named Team. If no such Team exists, a team will be created with the given name. 
An empty string will not move nor create any teams

--

## TeamColor
The BrickColor of the team if it gets created.

--

## CheckpointTrigger
Will trigger the spawn position change once turned to true, then it will be set to false again. (This attribute is created in-studio)
