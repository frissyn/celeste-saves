# 🍓 Celeste Saves

📼 Research repository for documenting Celeste savefiles. The documentation will extensively cover all the savefile nodes and paths. Currently a work in progress, don't mind what's missing.

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

+ [SaveData](/docs/savedata.md#SaveData)
    + [Version](/docs/savedata.md#Version)
    + [Name](/docs/savedata.md#Name)
    + [Time](/docs/savedata.md#Time)
    + [LastSave](/docs/savedata.md#LastSave)
    + [CheatMode](/docs/savedata.md#CheatMode)
    + [VariantMode](/docs/savedata.md#VariantMode)
    + [Assists](/docs/savedata.md#Assists)
        + [GameSpeed](/docs/savedata.md#Assists)
        + [Invincible](/docs/savedata.md#Assists)
        + [DashMode](/docs/savedata.md#Assists)
        + [InfiniteStamina](/docs/savedata.md#Assists)
        + [MirrorMode](/docs/savedata.md#Assists)
        + [ThreeSixtyDashing](/docs/savedata.md#Assists)
        + [InvisibleMotion](/docs/savedata.md#Assists)
        + [NoGrabbing](/docs/savedata.md#Assists)
        + [LowFriction](/docs/savedata.md#Assists)
        + [SuperDashing](/docs/savedata.md#Assists)
        + [Hiccups](/docs/savedata.md#Assists)
        + [PlayAsBadeline](/docs/savedata.md#Assists)
    + [TheoSisterName](/docs/savedata.md#TheoSisterName)
    + [UnlockedAreas](/docs/savedata.md#UnlockedAreas)
    + [TotalDeaths](/docs/savedata.md#TotalDeaths)
    + [TotalStrawberries](/docs/savedata.md#TotalStrawberries)
    + [TotalGoldenStrawberries](/docs/savedata.md#TotalGoldenStrawberries)
    + [TotalJumps](/docs/savedata.md#TotalJumps)
    + [TotalWallJumps](/docs/savedata.md#TotalWallJumps)
    + [TotalDashes](/docs/savedata.md#TotalDashes)
    + [Flags](/docs/savedata.md#Flags)
    + [Poem](/docs/savedata.md#Poem)
    + [SummitGems](/docs/savedata.md#SummitGems)
    + [LastArea](/docs/savedata.md#LastArea)
    + [Area](/docs/savedata.md#Area)
        + [AreaStats](/docs/savedata.md#AreaStats)
            + [Modes](/docs/savedata.md#Modes)
                + [AreaModeStats](/docs/savedata.md#AreaModeStats)
                    + [Checkpoints](/docs/savedata.md#Checkpoints)
                    + [Strawberries](/docs/savedata.md#Strawberries)
                        + [EntityID](/docs/savedata.md#EntityID)


### Credits

+ [**frissyn**](https://github.com/frissyn) - project lead

+ [**Aurora**](https://github.com/AuroraKy) - contributed to the [FileTime](/docs/topics/filetime.md) Topic

+ **Mnstrman06** - contributed to the [FileTime](/docs/topics/filetime.md) and [Poem](/docs/topics/poem.md) Topics

+ **Hydro0** - donated her \[100% / 202\] Strawberries savefile for research