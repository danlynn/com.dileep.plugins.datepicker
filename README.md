# DatePicker Plugin for android and ios using PhoneGap / Cordova 3.3

## Installation

1) Make sure that you have [Node](http://nodejs.org/) and [Cordova CLI](https://github.com/apache/cordova-cli) or [PhoneGap's CLI](https://github.com/mwbrooks/phonegap-cli) or [Cordova Plugman](https://github.com/apache/cordova-plugman/) installed on your machine.

2) Add a plugin to your project using [PhoneGap CLI](https://github.com/mwbrooks/phonegap-cli):

```bash
phonegap local plugin add https://github.com/witpok/com.dileep.plugins.datepicker
```
3) Make sure, that your plugin is within `config.xml` of your app
Android
```xml
<feature name="DatePicker">
    <param name="android-package" value="com.dileep.plugins.datepicker.DatePickerPlugin"/>
</feature>
```

4) The `clobber` definition of the plugin is called `datePicker`. So you can reference to the plugin from anywhere in your code.

Example:

```js
// defining options
var datePicker = new DatePicker();

var options = {
  date: new Date(),
  mode: 'date'
};
// calling show() function with options and a result handler
datePicker.show(options, function(date){
  console.log("date result " + date);  
});
```

5) include `DatePicker.js` to your `index.html`, for example: 
```html
<script type="text/javascript" src="js/DatePicker.js"></script>
```

Check section ["Options"](#options) below to see all options.

## Options

### mode
The mode of the date picker.

Typ: `String` 

Values: `"date"` / `"time"` / `"datetime"`

Default: `'datetime'`

### date
Selected date.

Typ: `String`

Default: `new Date()`

### allowOldDates
Shows or hide dates earlier then selected date.

Typ: `Boolean`

Values: `true` / `false`

Default: `true`

### allowFutureDates
Shows or hide dates after selected date.

Typ: `Boolean`

Values: `true` / `false`

Default: `true`

## Requirements
- PhoneGap 3.0 or newer /Cordova 3.0 or newer
- Android/iOs
