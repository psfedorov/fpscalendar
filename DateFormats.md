## Supported date formats ##
There are 3 supported date formats at the moment:
  * native (DD.MM.YYYY),
  * database (YYYY-MM-DD),
  * american (MM/DD/YYYY).
## Your own date formats ##
Not enough for you? You may **easily** and **quickly** create your own date formats!
fpsCalendar has an object `fpsCalendar.dateFormats`, in which properties all date formats are stored.
To add your own date format you should make a new property in `fpsCalendar.dateFormats` assigning to it an object with **2 methods**:
  * `buildDate(year, month, day) => str`. It is used to get the representation of a date. The given arguments are year, month (in "human-style" numeration) and day. The method should return a string.
  * `extractDate(str) => [year, month, day]`. It is used to extract a date from it's string representation. The given argument is a date representation string. The method should return an Array containing year, month (in "human-style" numeration) and day.

Here is an example of code where a 'database' format is created.
```
fpsCalendar.dateFormats['database'] = {
    'extractDate': function (str) {
        var d = str.split('-');
        if (d.length == 3) {
            return [parseInt(d[0]), parseInt(d[1]), parseInt(d[2])];
        }
        else {
            d = new Date();
            return [d.getFullYear(), d.getMonth() + 1, d.getDate()];
        }
    },
    'buildDate': function (year, month, day) {
        return year.toPaddedString(4) + '-' + month.toPaddedString(2) + '-' + day.toPaddedString(2);
    }
}
```