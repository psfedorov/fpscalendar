## fpsCalendar common parameters ##

Common parameters are customized by calling the function `fpsCalendar.setParams` with an object containing needed parameters as an argument:
```
fpsCalendar.setParams({calendarImg: '/media/img/calendar.jpg', firstDayOfWeek: 0, fadeInTime: 400});
```
Here is a list of all available parameters:
  * `calendarImg` - string containing a link to an image of a calendar. Default is `'fpscalendar.png'`.
  * `daysOfWeek` - array with abbreviations of names of week days starting with Sunday. Default is `['SU', 'MO', 'TU', 'WE', 'TH', 'FR', 'SA']`.
  * `firstDayOfWeek` - number of the first day of a week (from 0 to 6). Default is `1` (Monday).
  * `months` - array with names of months starting with January. Default is `['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']`.
  * `clearText` - string containing the text of the "clear" link. Default is `'Clear'`.
  * `fadeInTime` - time, which takes fpsCalendar box to completely appear (number in milliseconds). Default is `300`. `Note`: a "fade in" effect doesn't work in IE.
  * `defaultDateFormat` - string containing the name of the date format, which will be used for elements if no other date format was provided by user. Default is `'native'`.
  * `defaultEmptyValue` - string containing the default value for containers (which is inserted when the user clicks the "clear" link). Default is `empty string`.
  * `defaultYearRange` - array of two integer numbers, which defines the year range (- and +) in the year selection element. Default is `[90, 10]`.