# Celeste Saves

📼 Research repository for documenting Celeste savefiles. The documentation will extensively cover all the savefile nodes and paths. Currently a work in progress, don't mind what's missing.

### Preliminary Information

* Celeste savefiles are located at `Celeste/Saves/`
  * The location of the game folder depends on your vendor (`Steam`, `Epic Games`, etc.)
* Savefiles are denoted by the `.celeste` extension
  * The `Celeste/Saves/` folder by default contains up to three savefiles
    * Starting at `0`, each file represents a save in the displayed order
    * `0` for the first save, `1` for the second, etc.
    * Celeste will display extra savefiles, provided they are numbered correctly.
  * The numbered savefile might not exist if the save has not been created in-game. (or it could be empty)
* Savefiles are read, written, and parsed as XML 1.0[\*\*](https://www.w3.org/TR/xml/) files
* Savefiles can be edited manually to alter game behavior, stats, unlocks, etc.
* Celeste does not run save file validations (as far as I have tested), so invalid values will either be ignored or cause abnormal game behavior.
  * _i.e_ setting `TotalStrawberries` to an integer that is not the sum of each chapter's collected strawberries
  * _i.e_ setting `LastSave` to a FileTime before the supported epoch.

### Documentation Tree

Documentation of the savefile XML elements are listed in alphabetical order under [SaveData](savedata.md). In-depth explorations of some elements or attributes can be found under [Topics](./#Topics). Brush up on savefile terminology and definitions in the [Glossary](glossary.md).

### Credits

* [**frissyn**](https://github.com/frissyn) - Project Lead
* [**Aurora**](https://github.com/AuroraKy) - Contributed to the [FileTime](topics/filetime.md) Topic
* **Mnstrman06** - Contributed to the [FileTime](topics/filetime.md) and [Poem](topics/poem.md) Topics
* **Hydro0** - Donated her \[115% / 202 Strawberries] savefile for research
* **The Celeste Discord Community** - Contributing general game and savefile knowledge, thanks to the amazing people in there!

### Related Projects

* [frissyn/berrydeck](https://github.com/frissyn/berrydeck) - Celeste Savefile Editor
* [EverestAPI/Everest](https://github.com/EverestAPI/Everest) - Celeste Mod Loader
* [CelestialCartographers/Loenn](https://github.com/CelestialCartographers/Loenn) - (Better) Celeste Map Editor
* [CelestialCartographers/Ahorn](https://github.com/CelestialCartographers/Ahorn) - Celeste Map Editor
