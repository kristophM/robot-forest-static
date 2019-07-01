---
title: "Dates"
date: 2019-06-23T22:29:20-04:00
draft: true
sort_key: 13
category: "Python"
---

# Python Dates and Time

Dates and Time are a big topic in every language. Python does not consider dates
and times to be native types but includes a built-in `datetime` module that can
be imported.

## Creating a DateTime Object

A `datetime` object is constructed by calling `datetime` with the year, month, and
day as arguments. You can further specify hours, minutes, and seconds.

```python
import datetime
bday = datetime.datetime(1912, 6, 23)
print("Alan Turing's birthday was: ", bday)

lunch_appointment = datetime.datetime(2022, 1, 17, 13, 0, 0)
print("Our lunch appointment is for: ", lunch_appointment)
```

NOTE: `datetime` objects are stored as "timezone-unaware" unless you specify
a timezone.

### Current DateTime

The current date and time can be obtained easily with the `now()` function.

```python
import datetime
bday = datetime.datetime.now()
print("The current date and time is: ", bday)
```

## Formatting Dates and Times

The above datetime objects print in quite a long and ugly format. If you would like to
represent it in a more human readable format, you can use Python's built-in
`strftime()` method (short for "string format time"). This method takes the given
`datetime` and formats it according to whatever directives you pass in the string
argument.

```python
import datetime
d = datetime.datetime.now()

yymmdd = d.strftime("%Y-%m-%d")
day_of_week = d.strftime("%A")
proper_english_date = d.strftime("%B %d, %Y")

print(yymmdd)
print(day_of_week)
print(proper_english_date)
```

### Directives for `strftime()`

| Directive | Description                                     | Example                      |
|----|-------------------------------------------------------------|--------------------------|
| %a | Weekday, short version                                      | Wed                      |
| %A | Weekday, full version                                       | Wednesday                |
| %w | Weekday as a number 0-6, 0 is Sunday                        | 3                        |
| %d | Day of month 01-31                                          | 31                       |
| %b | Month name, short version                                   | Dec                      |
| %B | Month name, full version                                    | December                 |
| %m | Month as a number 01-12                                     | 12                       |
| %y | Year, short version, without century                        | 18                       |
| %Y | Year, full version                                          | 2018                     |
| %H | Hour 00-23                                                  | 17                       |
| %I | Hour 00-12                                                  | 5                        |
| %p | AM/PM                                                       | PM                       |
| %M | Minute 00-59                                                | 41                       |
| %S | Second 00-59                                                | 8                        |
| %f | Microsecond 000000-999999                                   | 548513                   |
| %z | UTC offset                                                  | +0100                    |
| %Z | Timezone                                                    | CST                      |
| %j | Day number of year 001-366                                  | 365                      |
| %U | Week number of year, Sunday as the first day of week, 00-53 | 52                       |
| %W | Week number of year, Monday as the first day of week, 00-53 | 52                       |
| %c | Local version of date and time                              | Mon Dec 31 17:41:00 2018 |
| %x | Local version of date                                       | 12/31/18                 |
| %X | Local version of time                                       | 17:41:00                 |
| %% | A % character                                               | %                        |

## Unix Date + Time

Unix time, also known as _epoch time_, is a number defined as the number of seconds
since midnight on January 1, 1970. It is a simpler way to represent time and
is often utilized on servers and databases to reduce ambiguity and simplify the
data.

```python
import datetime
d = datetime.datetime.now()
unix_time = d.timestamp()
print("no. of seconds since 1970", unix_time)

d1971 = datetime.utcfromtimestamp(3600 * 24 * 365)
print("One year after 1970: ", d1971)
```

## Dates vs. Date + Time vs. Time

It's important to understand the difference between dates and a date with a time.
When someone mentions July 1st, 2018 as a date, it's unclear what `datetime`
that would represent. Why? Because it can simultaneously be July 1st in, say,
New York, and July 2nd in Berlin due to time zones.

Thus, when storing datetime information in variables and databases using Python,
it's a good practice to specify a timezone (preferably UTC) to eliminate ambiguity.

```python
from pytz import timezone
import datetime
d = datetime.datetime(2022, 12, 1, 13, 45, tzinfo=pytz.utc)
print(d.isoformat())
```

### Time

Lastly, *time* as it pertains to Python describes the (local) time of day,
independent of any particular day.

```python
from datetime import time
lunch_time = time(12,30)
print(lunch_time.isoformat())
```

Notice that the time printed is simply a time, and not tied to any particular day.
