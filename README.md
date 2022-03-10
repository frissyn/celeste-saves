# 🍓 Celeste Saves

📼 Research repository for documenting Celeste savefiles. The documentation will extensively cover all the savefile nodes and paths. Currently a work in progress, don't mind what's missing.

**Related Projects:**

+ [frissyn/berrydeck](https://github.com/frissyn/berrydeck)
+ [frissyn/celeste.rb](https://github.com/frissyn/celeste.rb)

### Preliminary Information

+ Celeste savefiles are located at `Celeste/Saves/`
    + The location of the game folder depends on your vendor (`Steam`, `Epic Games`, etc.)
+ Savefiles are denoted by the `.celeste` extension
    + The `Celeste/Saves/` folder by default contains up to three savefiles
        + Starting at `0`, each file represents a save in the displayed order
        + `0` for the first save, `1` for the second, etc.
        + Celeste will display extra savefiles, provided they are numbered correctly.
    + The numbered savefile might not exist if the save has not been created in-game. (or it could be empty)
+ Savefiles are read, written, and parsed as XML 1.0[**](https://www.w3.org/TR/xml/) files
+ Savefiles can be edited manually to alter game behavior, stats, unlocks, etc.
+ Celeste does not run save file validations (as far as I have tested), so invalid values will either be ignored or cause abnormal game behavior.
    + *i.e* setting `TotalStrawberries` to an integer that is not the sum of each chapter's collected strawberries
    + *i.e* setting `LastSave` to a FileTime before the supported epoch.

### Documentation Tree

Documentation of the savefile XML elements are listed in alphabetical order under [Index](#Index). In-depth explorations of some elements or attributes can be found under [Topics](#Topics).

**Topics:**

+ [Areas](/docs/topics/areas.md)
+ [Entities](/docs/topics/entity.md)
+ [FileTime](/docs/topics/filetime.md)
+ [Poem](/docs/topics/poem.md)

**Index:**

+ [SaveData](/docs/savedata.md#Areas)
    + [Areas](/docs/savedata.md#Areas)
        + [AreaStats](/docs/savedata.md#AreaStats)
            + [Modes](/docs/savedata.md#Modes)
            + [AreaModeStats](/docs/savedata.md#AreaModeStats)
              + [Checkpoints](/docs/savedata.md#Checkpoints)
              + [Strawberries](/docs/savedata.md#Strawberries)
    + [Assists](/docs/savedata.md#Assists)
        + [DashMode](/docs/savedata.md#Assists)
        + [GameSpeed](/docs/savedata.md#Assists)
        + [Hiccups](/docs/savedata.md#Assists)
        + [InfiniteStamina](/docs/savedata.md#Assists)
        + [Invincible](/docs/savedata.md#Assists)
        + [InvisibleMotion](/docs/savedata.md#Assists)
        + [LowFriction](/docs/savedata.md#Assists)
        + [MirrorMode](/docs/savedata.md#Assists)
        + [NoGrabbing](/docs/savedata.md#Assists)
        + [PlayAsBadeline](/docs/savedata.md#Assists)
        + [SuperDashing](/docs/savedata.md#Assists)
        + [ThreeSixtyDashing](/docs/savedata.md#Assists)
    + [CheatMode](/docs/savedata.md#CheatMode)
    + [CurrentSession](/docs/savedata.md#CurrentSession)
        + [Area](/docs/savedata.md#Area)
        + [Audio](/docs/savedata.md#Audio)
            + [Ambience](/docs/savedata.md#Ambience)
            + [Music](/docs/savedata.md#Music)
            + [Parameters](/docs/savedata.md#Parameters)
        + [BeatBestTime](/docs/savedata.md#BeatBestTime)
        + [Counters](/docs/savedata.md#Counters)
        + [DoNotLoad](/docs/savedata.md#DoNotLoad)
        + [Flags](/docs/savedata.md#Flags)
        + [FurthestSeenLevel](/docs/savedata.md#FurthestSeenLevel)
        + [Inventory](/docs/savedata.md#Inventory)
            + [Backpack](/docs/savedata.md#Backpack)
            + [Dashes](/docs/savedata.md#Dashes)
            + [DreamDash](/docs/savedata.md#DreamDash)
            + [NoRefills](/docs/savedata.md#NoRefills)
        + [Keys](/docs/savedata.md#Keys)
        + [LevelFlags](/docs/savedata.md#LevelFlags)
        + [OldStats](/docs/savedata.md#AreaStats)
        + [RespawnPoint](/docs/savedata.md#RespawnPoint)
        + [Strawberries](/docs/savedata.md#Strawberries)
        + [SummitGems](/docs/savedata.md#SummitGems)
        + [UnlockedCSide](/docs/savedata.md#UnlockedCSide)
    + [Flags](/docs/savedata.md#Flags)
    + [LastArea](/docs/savedata.md#LastArea)
    + [LastSave](/docs/savedata.md#LastSave)
    + [Name](/docs/savedata.md#Name)
    + [Poem](/docs/savedata.md#Poem)
    + [SummitGems](/docs/savedata.md#SummitGems)
    + [TheoSisterName](/docs/savedata.md#TheoSisterName)
    + [Time](/docs/savedata.md#Time)
    + [TotalDashes](/docs/savedata.md#TotalDashes)
    + [TotalDeaths](/docs/savedata.md#TotalDeaths)
    + [TotalGoldenStrawberries](/docs/savedata.md#TotalGoldenStrawberries)
    + [TotalJumps](/docs/savedata.md#TotalJumps)
    + [TotalStrawberries](/docs/savedata.md#TotalStrawberries)
    + [TotalWallJumps](/docs/savedata.md#TotalWallJumps)
    + [UnlockedAreas](/docs/savedata.md#UnlockedAreas)
    + [VariantMode](/docs/savedata.md#VariantMode)
    + [Version](/docs/savedata.md#Version)

### Credits

+ [**frissyn**](https://github.com/frissyn) - project lead

+ [**Aurora**](https://github.com/AuroraKy) - contributed to the [FileTime](/docs/topics/filetime.md) Topic

+ **Mnstrman06** - contributed to the [FileTime](/docs/topics/filetime.md) and [Poem](/docs/topics/poem.md) Topics

+ **Hydro0** - donated her \[115% / 202 Strawberries\] savefile for research
