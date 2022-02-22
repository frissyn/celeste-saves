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
    + The numbered savefile might not exist if the save save has not been created in-game. (or it could be empty)
+ Savefiles are read, written, and parsed as [XML 1.0](https://www.w3.org/TR/xml/) files
+ Savefiles can be edited manually to alter game behavior, stats, unlocks, etc.
+ Celeste does not run save file validations (as far as I have tested), so invalid values will either be ignored or cause abnormal game behavior.
    + *i.e* setting `TotalStrawberries` to an integer that is not the sum of each chapter's collected strawberries
    + *i.e* setting `LastSave` to a FileTime before the supported epoch.

### Documentation Tree

+ [SaveData](tree/master/docs/savedata.md)
    - [Version](tree/master/docs/savedata.md#Version)
    - [Name](tree/master/docs/savedata.md#Name)
    - [Time](tree/master/docs/savedata.md#Time)
    - [LastSave](tree/master/docs/savedata.md#LastSave)
    - [CheatMode](tree/master/docs/savedata.md#CheatMode)
    - [VariantMode](tree/master/docs/savedata.md#VariantMode)
    - [Assists](tree/master/docs/savedata.md#Assists)
        + [GameSpeed](tree/master/docs/savedata.md#GameSpeed)
        + [Invincible](tree/master/docs/savedata.md#Invincible)
        + [DashMode](tree/master/docs/savedata.md#DashMode)
        + [InfiniteStamina](tree/master/docs/savedata.md#InfiniteStamina)
        + [MirrorMode](tree/master/docs/savedata.md#MirrorMode)
        + [ThreeSixtyDashing](tree/master/docs/savedata.md#ThreeSixtyDashing)
        + [InvisibleMotion](tree/master/docs/savedata.md#InvisibleMotion)
        + [NoGrabbing](tree/master/docs/savedata.md#NoGrabbing)
        + [LowFriction](tree/master/docs/savedata.md#LowFriction)
        + [SuperDashing](tree/master/docs/savedata.md#SuperDashing)
        + [Hiccups](tree/master/docs/savedata.md#Hiccups)
        + [PlayAsBadeline](tree/master/docs/savedata.md#PlayAsBadeline)
    - [TheoSisterName](tree/master/docs/savedata.md#TheoSisterName)
    - [UnlockedAreas](tree/master/docs/savedata.md#UnlockedAreas)
    - [TotalDeaths](tree/master/docs/savedata.md#TotalDeaths)
    - [TotalStrawberries](tree/master/docs/savedata.md#TotalStrawberries)
    - [TotalGoldenStrawberries](tree/master/docs/savedata.md#TotalGoldenStrawberries)
    - [TotalJumps](tree/master/docs/savedata.md#TotalJumps)
    - [TotalWallJumps](tree/master/docs/savedata.md#TotalWallJumps)
    - [TotalDashes](tree/master/docs/savedata.md#TotalDashes)
    - [Flags](tree/master/docs/savedata.md#Flags)
    - [Poem](tree/master/docs/savedata.md#Poem)
    - [SummitGems](tree/master/docs/savedata.md#SummitGems)
    - [LastArea](tree/master/docs/savedata.md#LastArea)
    - [Area](tree/master/docs/savedata.md#Area)
        + [AreaStats](tree/master/docs/savedata.md#AreaStats)
            - [Modes](tree/master/docs/savedata.md#Modes)
                + [AreaModeStats](tree/master/docs/savedata.md#AreaModeStats)
                    - [Checkpoints](tree/master/docs/savedata.md#Checkpoints)
                    - [Strawberries](tree/master/docs/savedata.md#Strawberries)
                        + [EntityID](tree/master/docs/savedata.md#Version)
