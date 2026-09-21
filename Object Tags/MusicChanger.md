---
title: MusicChanger
parent: Object Tags
---

# MusicChanger
{: .no_toc }
Music changers allow you to change or modify your currently playing music! Your songs should be inside of the "Music" SoundGroup and be named properly. Also, these songs can have a `MusicName` string attribute, which will appear when using the `;music` chat command!

## On this page
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Attributes

| AttributeName | Value | Default |
|---------------|-------|---------|
| [SoundName](#soundname) | `string` | `"N/A"` |
| [SyncTime](#synctime) | `boolean` | `false` |
| [StopOtherSongs](#stopothersongs) | `boolean` | `true` |
| [PlaybackSpeed](#playbackspeed) | `number` | `1` |
| [Volume](#volume) | `number` | `1` |
| [ChangeMusicTrigger](#changemusictrigger) | `bool` | `false` |

---

## Sounds

| SoundName | Condition |
|----------|---------|
| TriggerSound | Plays on trigger. |

---

# Attributes

---

## SoundName
The name of the sound from the Music folder will the MusicChanger change to, this will become the `currentSound`. if SoundName is the same as `currentSound`, the song wont change but things like [Volume](#volume) and [PlaybackSpeed](#playbackspeed) will still be applied.

---

## SyncTime
When changing the song, its `TimePosition` will be the same as the previous song.

---

## StopOtherSongs
Whether or not the previous songs should stop when the sound changes

---

## PlaybackSpeed
Will change the PlaybackSpeed property of the `currentSound`

---

## Volume
Will change the Volume property of the `currentSound`

---

## ChangeMusicTrigger
Will trigger the sound change once turned to true, then it will be set to false again. (This attribute is created in-studio)

---



