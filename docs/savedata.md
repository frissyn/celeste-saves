# SaveData

The Celeste savefile is written and parsed in the XML 1.0[**](https://www.w3.org/TR/xml/) file format. All relevant elements are children under the `SaveData` parent element. The `SaveData` element declares two XML namespaces:

```xml
<SaveData xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
```

The following documentation covers all child elements of the `SaveData` element.

#### Version

Version of the Celeste game and client. `1.4.0.0` is currently the latest Celeste version. Is a `string` value.

Example:
```xml
<Version>1.4.0.0</Version>
```

#### Name

Name of the savefile in Celeste. Defaults to `Madeline`. Is a `string` value.

```xml
<Name>Madeline</Name>
```

### Time

Total duration of time spent playing Celeste. Measured in 100 nanosecond intervals since January 1, 1601 (UTC) as per the Win32 FileTime[**](https://docs.microsoft.com/en-us/windows/win32/api/minwinbase/ns-minwinbase-filetime) specification. See the [FileTime](/docs/topics/filetime.md) topic for more details. Is an `integer` value. This number is recorded with uneccessary precision.

```xml
<Time>8650037750000</Time>
```

**Note:** This has only been tested on the PC (Windows) version of Celeste, and may differ on other operating systems. Feel free to contribute!

### LastSave

UTC timestamp representing the last time the game has written new data to the savefile. Is a `string` value.

```xml
<LastSave>0001-01-01T00:00:00</LastSave>
```

### CheatMode

Whether [Cheat Mode](https://celestegame.fandom.com/wiki/Cheat_Mode) is enabled on the savefile. Is a `boolean` value. Can be `0`, `1`, `true`, or `false`.

```xml
<CheatMode>true</CheatMode>
```

### AssistMode

Whether [Assist Mode](https://celestegame.fandom.com/wiki/Variant_Mode#Assists) is enabled on the savefile. Is a `boolean` value. Can be `0`, `1`, `true`, or `false`. Uses [Assists](#Assists) to determine what assists are enabled or disabled.

```xml
<AssistMode>true</AssistMode>
```

### VariantMode

Whether [Variant Mode](https://celestegame.fandom.com/wiki/Variant_Mode) is enabled on the savefile. Is a `boolean` value. Can be `0`, `1`, `true`, or `false`. Uses [Assists](#Assists) to determine what assists are enabled or disabled.

```xml
<VariantMode>true</VariantMode>
```
