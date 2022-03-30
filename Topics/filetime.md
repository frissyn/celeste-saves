# Topic :: FileTime

**Note:** These notes assume that Celeste is running on Windows. If you play on Mac or Linux, please feel free to contribute!

`Time` is an an element that appears on numerous occassions in the Celeste savefile, usually denoting a **duration** of playtime. After extensive calculations and testing [(cc)](/README.md#credits), it was determined that this value is a 64-bit integer representing 100-nanosecond intervals since January 1, 1601. [\[1\]](https://documentation.help/Far-Manager/filetime.html) This is the standard structure that Win32 uses to determine time. [\[2\]](https://docs.microsoft.com/en-us/windows/win32/api/minwinbase/ns-minwinbase-filetime)

Within our context of measuring playtime, we can ignore the epoch (Jan 1, 1601), and reduce the measurement to `10,000 units per ms`. 

$$milliseconds = filetime / 10000$$

For example, the FileTime `864000000000` translates to `86400000` milliseconds, which is exactly 24 hours.

If you were to put that in a Savefile:

```xml
<Time>864000000000</Time>
```

Celeste would display `24:00:00.000` on the savefile associated with that time.

So, interpreting this value in other languages (besides C, C++, and C# which have native implementations of `FileTime` on Windows), can be done by dividing the value by `10,000` and reading that into a naïve datetime in your language of choice as milliseconds. (Or a time delta, which is more convinent in this context.)

**Code Samples:**

{% tabs %} {% tab title="Python" %}

```python
>>> import datetime as dt
>>> units = 864000000000
>>> delta = dt.timedelta(milliseconds=units // 10000)
>>> delta.days
1
```

{% endtab %}

{% tab title="Ruby" %}

```ruby
irb(main):001:0> require 'time'
irb(main):002:0> units = 864000000000
irb(main):003:0> time = Time.at units / 10000 / 1000
irb(main):004:0> time.to_i / 86400
=> 1
```

{% endtab %} {% endtabs %}