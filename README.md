# winston-rotate-file

[![NPM](https://nodei.co/npm/winston-rotate-file.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/winston-rotate-file/)

A transport for winston which logs to a rotating file.

## Usage

``` js
  winston.add(require('winston-rotate-file'), options)
```

The RotateFile transport can rotate files by minute, hour, day, month or year. In addition to the options accepted by the File transport, the Rotate File Transport also accepts the following options:

* __datePattern:__ A string representing the pattern to be used when appending the date to the filename (default '.yyyy-MM-dd'). The meta characters used in this string will dictate the frequency of the file rotation. For example, if your datePattern is simply '.HH' you will end up with 24 log files that are picked up and appended to every day.
* __prepend:__ Defines if the rolling time of the log file should be prepended at the begging of the filename (default `false`)
* __preserveExt:__ Defines if the rolling time of the log file should be appended to the filename while preserving the file extension (default `false`)

Valid meta characters in the datePattern are:

* __yy:__ Last two digits of the year.
* __yyyy:__ Full year.
* __M:__ The month.
* __MM:__ The zero padded month.
* __d:__ The day.
* __dd:__ The zero padded day.
* __H:__ The hour.
* __HH:__ The zero padded hour.
* __m:__ The minute.
* __mm:__ The zero padded minute.

*Metadata:* Logged via util.inspect(meta);

##### LICENSE: MIT
##### AUTHOR: [Charlie Robbins](https://github.com/indexzero)
##### MAINTAINER: [Matt Berther](https://github.com/mattberther)
