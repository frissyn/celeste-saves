# Topic :: Poem

The `Poem` element in the Celeste savefile denotes a list of string elements, each being an abbreaviation for the game's journal (reffered to in the savefile as `poem`).

Each chapter has a 1-2 letter abbreviation, and another abbreviation followed by `r` for `remix`, which is what the savefile uses to refer to B-Sides and/or C-Sides.

A player's savefile poem might look like this:

```xml
<Poem>
  <string>fc</string>
  <string>cr</string>
  ...
</Poem>
```

Which means they have both Chapter 1 and Chapter 3's Crystal Heart.

### Reference Table

| Abbreviation | Chapter               | Name                  |
|:------------:|:----------------------|:----------------------|
| fc           | 1A - Forsaken City    | Pointless Machines    |
| fcr          | 1B - Forsaken City    | Sever the Skyline     |
| os           | 2A - Old Site         | Resurrections         |
| osr          | 2B - Old Site         | Black Moonrise        |
| cr           | 3A - Celestial Resort | Scattered and Lost    |
| crr          | 3B - Celestial Resort | Good Karma            |
| cs           | 4A - Golden Ridge     | Eye of the Storm      |
| csr          | 4B - Golden Ridge     | Golden Feather        |
| t            | 5A - Mirror Temple    | Quiet and Falling     |
| tr           | 5B - Mirror Temple    | Mirror Magic          |
| tf           | 6A - Reflection       | Heavy and Frail       |
| tfr          | 6B - Reflection       | Center of the Earth   |
| ts           | 7A - The Summit       | Pink Sunrise          |
| tsr          | 7B - The Summit       | No More Running       |
| mc           | 8A - Core             | Heart of the Mountain |
| mcr          | 8B - Core             | Say Goodbye           |
| fw? ll?      | 9 - Farewell          | Empty Space           |

**Note:** While Chapter 9 is assumed to be either `fw` (Farewell) or `ll` (LostLevels), it does not appear in the `Poem` upon completion.