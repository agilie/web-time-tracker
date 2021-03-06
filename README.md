[![License](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/agilie/Web-Time-Tracker)

# Web Time Tracker
Plugin named **Timetracker** is a time counter that works in both increase and decrease directions. It can be embedded in websites and used as a timer, tracker, counting down tool and in any other situation where you need to control elapsed time (for example, during online testing).
**Timetracker** plugin can be adapted to any web resource and designed in accordance with the website style.
For initialization, use the command:
```sh
$('.timetracker').timetracker();
```

# Timetracker format
The default interval is 1 second, the display format is in minutes and seconds. 
To customize time format use "format" field during initialization:
```sh
$('.timetracker').timetracker({'format': 'i:s'});
```

# How to use plugin
To specify when you want to stop the countdown, use the setting timestop (in seconds):
```sh
$('.timetracker').timetracker({'timestop': 15})
```
The parameter "countdown" allows you to specify the counting direction, and the parameter "timestop", in seconds, specifies the moment when the count should be stopped or resumed.
```sh
$('.timetracker').timetracker({'countdown': true, 'timestop': 60});
```
To guide the tracker, there are a number of events that allow you to start or stop counting and return to the original state.
```sh
$('.timetracker').timetracker('start');
$('.timetracker').timetracker('stop');
$('.timetracker').timetracker('reset');
```

You can assign your handler to process the timer stop event:
```sh
$('.timetracker').timetracker({
   'timestop': 5,
   'format': 'i:s',
   'stop': function() {
       alert('The timer stopped');
   }
});
```

# Example of tracker usage
Here we can show you an example of tracker usage: 
```sh
<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <title>Title</title>
   <script src="https://code.jquery.com/jquery-2.2.0.min.js"></script>
   <script src="../app/js/time-tracker.js"></script>
</head>
<body>
   <span class='timetracker'></span>
   <button onClick="javascript:$('.timetracker').timetracker('start');">start</button>
   <button onClick="javascript:$('.timetracker').timetracker('stop');">stop</button>
   <button onClick="javascript:$('.timetracker').timetracker('reset');">reset</button>
   <script>
       $('.timetracker').timetracker({'timestop': 15, 'format': 'i:s', 'countdown': true});
   </script>
</body>
</html>
```

## Troubleshooting
Problems? Check the [Issues](https://github.com/agilie/Web-Time-Tracker/issues) block 
to find the solution or create an new issue that we will fix asap. Feel free to contribute.

## Author
This jQuery plugin is open-sourced by [Agilie Team](https://www.agilie.com) ([info@agilie.com](mailto:info@agilie.com))

## Contributor
[Petr Simanko](https://github.com/PetrSimanko)

## Contact us
If you have any questions, suggestions or just need a help with web or mobile development, please email us at <web@agilie.com>. You can ask us anything from basic to complex questions. 

We will continue publishing new open-source projects. Stay with us, more updates will follow!

## License
The [MIT](https://github.com/agilie/Web-Time-Tracker/blob/master/LICENSE.md) License (MIT) Copyright © 2017 [Agilie Team](https://www.agilie.com)
