# Calendrical

## What is it?

Calendrical is a plugin for jQuery that provides popup date and time pickers inspired by Google Calender.

The time picker component allows the time separator to be omitted when entering the time via the keyboard, which allows for quicker data entry. The time separator will be automatically included when tabbing away from the time picker. For example entering '1300' will be converted to either '1:00pm' or '13:00' (depending on whether or not the `isoTime` option is set).

## Installation

Copy and include the JavaScript file `jquery.calendrical.js`, and the style sheet `calendrical.css` in your project.

If you use SASS for your project, you can include the code in `calendrical.scss` instead of the css file. If you want to change the color scheme for Calendrical, you can edit the color definitions in the scss file and then regenerate the css using `build_css.sh`.

## Usage

You can add Calendrical date and time pickers to your existing text fields using the following functions:

  * .calendricalDate
  * .calendricalTime
  * .calendricalDateRange
  * .calendricalTimeRange
  * .calendricalDateTimeRange
  
See `example.html` for examples of how to use these functions.

## Options

All of the Calendrical functions can accept an options hash as a parameter.

Available options:

  * __usa__ - Use USA-style middle endian dates (7/21/2010), instead of the default European-style little endian dates (21/7/2010).
  * __isoTime__ - Use 24-hour clock (ISO 8601) instead of default 12 hour clock with am/pm.
  * __defaultHour__ - Default hour to scroll the dropdown time select box to,
  if the field doesn't already have a time value when it's shown. Specify as an integer (0..23). Defaults to 9.
  * __minuteIncrement__ - Specify the minute increment for the time picker. Defaults to 30.
  * __timeSeparator__ - Specify the character used to separate the hour and minute components of the time. Valid options are `:`, `-`, `.` or `,`. Defaults to `:`.
  * __minimumTime__ - Specify the earliest time displayed in the time picker. Defaults to `{ hour: 0, minute: 0 }`.
  * __maximumTime__ - Specify the latest time displayed in the time picker. Defaults to `{ hour: 24, minute: 0}`.
  * __matchContainerWidth__ - If set to `true` then the width of the time picker drop down will match the width of the textbox that the time picker has been applied to. Defaults to `false`.
  * __canSpanMidnight__ - Specifies whether or not the time picker can span midnight if the combination of minimum and maximum times cross midnight. Defauls to `false`.