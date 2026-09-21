---
title: BehaviorUtil
nav_order: 2
---

# BehaviorUtil Documentation
{: .no_toc }

## On this page
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Functions

| Function | Returns |
|----------|---------|
| [getAttr](#getattr) | `T` |
| [getTriggerConfig](#gettriggerconfig) | `TriggerConfig` |
| [randomPlaybackSpeed](#randomplaybackspeed) | `number?` |
| [playSoundInstance](#playsoundinstance) | nothing |
| [playRandomSound](#playrandomsound) | `Sound?` |
| [playSound](#playsound) | `Sound?` |
| [setupSounds](#setupsounds) | `{ Sound }` |
| [setupTriggers](#setuptriggers) | `TriggerController` |

---

## getAttr

```lua
getAttr(instance: Instance, name: string, default: T): T
```

Looks for attribute called `[name]` inside `[instance]`, if it doesnt find it, return `[default]`

---

## getTriggerConfig

```lua
getTriggerConfig(instance: Instance): TriggerConfig
```

Sets up a TriggerConfiguration in `[instance]`. Tries to get any attributes from a child called TriggerConfiguration or the instance itself using these attributes:

| Attribute | Type | Description |
|-----------|------|-------------|
| Enabled | boolean | Should it even run? |
| TouchActivated | boolean | Should it be activated by touch (either by the local player or ANY object) |
| ClickActivated | boolean | Should it be activated by Click? (using a ClickDetector (its recommended u add a clickdetector beforehand if you want to configurate it such as the MaxActivationDistance)) |
| AllowPlayer | boolean | Should it be activated by the parts inside the Local players character? (only relevant if TouchActivated is true) |
| AllowedTags | string | List of tags that the touch event will check if the touched part has. formatted like this: `"tag1, tag2, tag3, ..."` |

---

## randomPlaybackSpeed

```lua
randomPlaybackSpeed(sound: Sound): number?
```

Changes a sounds `playbackSpeed` depending on the sounds `"RandomPlayback"` string attribute.
Can be formatted in 2 ways:

| Format | Example | Behavior |
|--------|---------|----------|
| Choice | `"x, y, z, ..."` | will choose one of the values |
| Range | `"x - y"` | will choose between the two values |

---

## playSoundInstance

```lua
playSoundInstance(sound: Sound?)
```

Plays the sound, it also looks for attributes:

| Attribute | Type | Description |
|-----------|------|-------------|
| Global | boolean | if true, a clone of the sound is put inside SoundService to play in the players Mind... |
| RandomPlayback | string | changes the PlaybackSpeed (read `BehaviorUtil.randomPlaybackSpeed`) |

---

## playRandomSound

```lua
playRandomSound(sounds: { Sound }): Sound?
```

Plays random sound from a table made of Sounds (Will support the Global and RandomPlayback attributes)

---

## playSound

```lua
playSound(instance: Instance, soundName: string): Sound?
```

Different from `playSoundInstance`, it will check for a sound named `[soundName]` inside `[instance]`. Will play a random one if theres multiple sounds named the same (Will support the Global and RandomPlayback attributes)

---

## setupSounds

```lua
setupSounds(part: Instance, folderName: string?): { Sound }
```

Looks for a Sounds folder (doesnt necessarily need to be a folder) named `folderName` (or named `"Sounds"` as default) inside `part` and returns a table with every Sound Instance.

---

## setupTriggers

```lua
setupTriggers(instance: Instance, triggerAttrName: string?, callback: (triggerSource: Instance?) -> ()): TriggerController
```

Sets up triggers on [instance] using TriggerConfiguration. Also adds certain attributes to an Object (if given):

| Attribute | Type | Description |
|-----------|------|-------------|
| OneTimeUse | boolean | if true, the trigger will only fire once |
| Cooldown | number | seconds to wait before the trigger can fire again |
| triggerAttrName | boolean | For this one, you have to set it up with the `triggerAtrrName `parameter. It will be a bool value that once set to true, will trigger the callback then get set to false again. (useful for button interactions!) |
