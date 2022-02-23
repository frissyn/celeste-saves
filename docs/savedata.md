# SaveData

The Celeste savefile is written and parsed in the XML 1.0[**](https://www.w3.org/TR/xml/) file format. All relevant elements are children under the `SaveData` parent element. The `SaveData` element declares two XML namespaces:

```xml
<SaveData xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
```

The following documentation covers all child elements of the `SaveData` element.

### Ambience

🚧 Documentation coming soon!

### Area

🚧 Documentation coming soon!

### AreaModeStats

🚧 Documentation coming soon!

### AreaStats

🚧 Documentation coming soon!

### Areas

🚧 Documentation coming soon!

### AssistMode

Whether [Assist Mode](https://celestegame.fandom.com/wiki/Variant_Mode#Assists) is enabled on the savefile. Is a `boolean` value. Uses [Assists](#Assists) to determine what assists are enabled or disabled.

```xml
<AssistMode>true</AssistMode>
```

### Assists

List of child elements that determine what variants and assist mechanics are enabled or disabled. Each child element is a `boolean` value, with the exception of `GameSpeed` (`integer`), and `DashMode` (`string`).

+ GameSpeed: *How fast the game moves. Valid range of integers is unkown.*
+ Invincible: *Enable or disable player invincibility.*
+ DashMode: *What dash mode the player uses. Is a `string` value, defaults to `Normal`. Valid values are for `2` and `Infinite` are currently unknown.*
+ DashAssist: *Enable or disable dash assist.*
+ InfiniteStamina: *Give the player infinite stamina.*
+ MirrorMode: *Enable or disable enable mirror mode.*
+ ThreeSixtyDashing: *Enable or disable enable 360° dashing.*
+ InvisibleMotion: *Hide the player's sprite in-game.*
+ NoGrabbing: *Enable or disable the ability to grab walls.*
+ LowFriction: *Make the floor and walls slippery.*
+ SuperDashing: *Enable or disable super dashing.*
+ Hiccups: *Enable or disable player hiccups.*
+ PlayAsBadeline: *Change the player's sprite to Badeline.*


```xml
<Assists>
  <GameSpeed>10</GameSpeed>
  <Invincible>false</Invincible>
  <DashMode>Normal</DashMode>
  <DashAssist>false</DashAssist>
  ...
</Assists>
```

### Backpack

🚧 Documentation coming soon!

### BeatBestTime

🚧 Documentation coming soon!

### CheatMode

Whether [Cheat Mode](https://celestegame.fandom.com/wiki/Cheat_Mode) is enabled on the savefile. Is a `boolean` value.

```xml
<CheatMode>true</CheatMode>
```

### Checkpoints

🚧 Documentation coming soon!

### CurrentSession

🚧 Documentation coming soon!

### Dashes

🚧 Documentation coming soon!

### DoNotLoad

🚧 Documentation coming soon!

### DreamDash

🚧 Documentation coming soon!

### EntityID

Denotes a collectible of some kind (berries, keys, etc.), usually stored as a list of child elements under a parent element.
Has one attribute, `KEY`. See the [Entities](/docs/topics/entity.md) Topic for more detailed info.
 
```xml
<EntityID Key="end:4"/>
```

### Flags

List of of string elements denoting story events that affect dialouge trees. The Chapter 5 and 6 A-Side intro are affected by these flags. There are currently only two known flags that affect dialouge.

```xml
<Flags>
  <string>MetTheo</string>
  <string>TheoKnowsName</string>
  ...
</Flags>
```

### FurthestSeenLevel

🚧 Documentation coming soon!

### Inventory

🚧 Documentation coming soon!

### Keys

🚧 Documentation coming soon!

### LastArea

The last area (Chapter) the player has opened or played. The Chapter Selection screen will open to this area. This element has no value, and is instead denoted by its attributes.

```xml
<LastArea ID="0" Mode="Normal" SID="Celeste/0-Intro"/>
```

### LastSave

UTC timestamp representing the last time the game has written new data to the savefile? (see note) Is a `string` value.

```xml
<LastSave>0001-01-01T00:00:00</LastSave>
```

**Note:** After some testing and recording, it appears this value remains the same across different savefiles no matter when they were created or opened in-game. It's purpose is unclear and only an educated guess. Feel free to contribute!

### LevelFlags

🚧 Documentation coming soon!

### Modes

🚧 Documentation coming soon!

### Music

🚧 Documentation coming soon!

### NoRefills

🚧 Documentation coming soon!

### OldStats

🚧 Documentation coming soon!

### Parameters

🚧 Documentation coming soon!

### Poem

List of string elements that contain Chapter name abbreviations, denoting which Crystal Hearts have been unlocked. See the [Poem](/docs/topics/peom.md) Topic for more details.

```xml
<Poem>
  <string>cs</string>
  <string>os</string>
  <string>fc</string>
  <string>mc</string>
  ...
</Poem>
```

### RespawnPoint

🚧 Documentation coming soon!

### RevealedChapter9

Whether or not the Chapter 9 (Farewell) has been revealed to the player on the Chapter Selection screen. Is a `boolean` value. Defaults to `false`.

```xml
<RevealedChapter9>true</RevealedChapter9>
```

### Strawberries

List of child [EntityID](/docs/savedata.md#EntityID)s denoting strawberry collectibles. Normally found in [AreaModeStats](/docs/savedata.md#AreaModeStats) to save which strawberries have been collected and in what order.

```xml
<Strawberries>
  <EntityID Key="2:11"/>
  <EntityID Key="3:9"/>
  <EntityID Key="3b:2"/>
  ...
</Strawberries>
```

### SummitGems

List of 6 boolean elements denoting which Summit Gems have been obtained, in order. Each element is a `boolean` value.

```xml
<SummitGems>
  <boolean>true</boolean> <!--- Blue Star --->
  <boolean>true</boolean> <!--- Turquoise Square --->
  <boolean>true</boolean> <!--- Green Hexagon --->
  <boolean>true</boolean> <!--- Yellow Circle --->
  <boolean>true</boolean> <!--- Pink Diamond (Steven Universe reference??) --->
  <boolean>true</boolean> <!--- White Circle --->
</SummitGems>
```

### TheoSisterName

The name of Theo's sister. Affects his dialouge in Chapter 6 (A-Side). Is a `string` value. Defaults to `Alex`.

```xml
<TheoSisterName>Alex</TheoSisterName>
```

### Time

Total duration of time spent playing Celeste. Measured in 100 nanosecond intervals since January 1, 1601 (UTC) as per the Win32 FileTime[**](https://docs.microsoft.com/en-us/windows/win32/api/minwinbase/ns-minwinbase-filetime) specification. See the [FileTime](/docs/topics/filetime.md) Topic for more details. Is an `integer` value. This number is recorded with uneccessary precision.

```xml
<Time>8650037750000</Time>
```

**Note:** This has only been tested on the PC (Windows) version of Celeste, and may differ on other operating systems. Feel free to contribute!

### TotalDashes

Number of dashes the player has done. In an `integer` value. Defaults to `0`.

```xml
<TotalDashes>251592</TotalDashes>
```

### TotalDeaths

Number of deaths the player has. Is an `integer` value. Defaults to `0`.

```xml
<TotalDeaths>10</TotalDeaths>
```

### TotalGoldenStrawberries

Number of golden strawberries the player has. Is an `integer` value. Defaults to `0`.

```xml
<TotalGoldenStrawberries>26</TotalGoldenStrawberries>
```

### TotalJumps

Number of jumps the player has inputted. Is an `integer` value. Defaults to `0`. It's unclear if this number excludes wall jumps.

```xml
<TotalJumps>76587</TotalJumps>
```

### TotalStrawberries

Number of strawberries the player has. Is an `integer` value. Defaults to `0`.

```xml
<TotalStrawberries>202</TotalStrawberries>
```

### TotalWallJumps

Number of wall jumps the player has done. Is an `integer` value. Defaults to `0`.

```xml
<TotalStrawberries>20918</TotalStrawberries>
```

**Note:** It is unclear if neutral jumps add to this counter. Feel free to contribute!

### UnlockedAreas

Number of area (chapters) that the player has unlocked. Is an `integer` value. Defaults to `1`.

```xml
<UnlockedAreas>10</UnlockedAreas>
```

### UnlockedCSide

🚧 Documentation coming soon!

### VariantMode

Whether [Variant Mode](https://celestegame.fandom.com/wiki/Variant_Mode) is enabled on the savefile. Is a `boolean` value. Uses [Assists](#Assists) to determine what variants are enabled or disabled.

```xml
<VariantMode>true</VariantMode>
```

#### Name

Name of the savefile in Celeste. Defaults to `Madeline`. Is a `string` value.

```xml
<Name>Madeline</Name>
```

#### SaveData

The Celeste savefile is written and parsed in the XML 1.0[**](https://www.w3.org/TR/xml/) file format. All relevant elements are children under the `SaveData` parent element. The `SaveData` element declares two XML namespaces:

```xml
<SaveData xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
```

The following documentation covers all child elements of the `SaveData` element.

#### Version

Version of the Celeste game and client. `1.4.0.0` is currently the latest Celeste version. Is a `string` value.

```xml
<Version>1.4.0.0</Version>
```
