# Topic :: FileTime

**Note:** These notes assume that Celeste is running on Windows. If you play on Mac or Linux, please feel free to contribute!

`Time` is an an element that appears on numerous occassions in the Celeste savefile, usually denoting a **duration** of playtime. After extensive calculations and testing [(cc)](/README.md#credits), it was determined that this value is a 64-bit integer representing 100-nanosecond intervals since January 1, 1601. [\[1\]](https://documentation.help/Far-Manager/filetime.html) This is the standard structure that Win32 uses to determine time. [\[2\]](https://docs.microsoft.com/en-us/windows/win32/api/minwinbase/ns-minwinbase-filetime)

Within our context of measuring playtime, we can ignore the epoch (Jan 1, 1601), and reduce the measurement to `10,000 units per ms`.  For example the FileTime `116445600000000000` translates to `86400000` milliseconds, which is exactly 24 hours.

This value:

```xml
<Time>116445600000000000</Time>
```

translates to 24 hours of playtime, and Celeste would display `24:00:00.00` on the savefile associated with that time.