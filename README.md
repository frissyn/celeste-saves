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

Documentation of the savefile XML elements are listed in alphabetical order under [SaveData](/savedata.md). In-depth explorations of some elements or attributes can be found under [Topics](#Topics).

### Credits

+ [**frissyn**](https://github.com/frissyn) - project lead

+ [**Aurora**](https://github.com/AuroraKy) - contributed to the [FileTime](/docs/topics/filetime.md) Topic

+ **Mnstrman06** - contributed to the [FileTime](/docs/topics/filetime.md) and [Poem](/docs/topics/poem.md) Topics

+ **Hydro0** - donated her \[115% / 202 Strawberries\] savefile for research

+ **The Celeste Discord Community** - Contributing general game and savefile knowledge.

### Related Projects

+ [frissyn/berrydeck](https://github.com/frissyn/berrydeck) - Celeste Savefile Editor
+ [EverestAPI/Everest](https://github.com/EverestAPI/Everest) - Celeste Mod Loader
+ [CelestialCartographers/Loenn](https://github.com/CelestialCartographers/Loenn) - (Better) Celeste Map Editor
+ [CelestialCartographers/Ahorn](https://github.com/CelestialCartographers/Ahorn) - Celeste Map Editor