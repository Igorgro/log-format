# Log format
This document describes the log format, which is used in my applications
## File name
Log file must be named as `<application name>.log`
## Log content
The format of log line is listed below
```
[DATE TIME][LOG LEVEL][THREAD] Message
```
The contracted format of log line for devices with line width less than 64 characters:
```
[DATE TIME][LOG LEVEL][THREAD]
Message
```
The parts of the log line:
* `DATE TIME` - Date/time in format: `YYYY-MM-DD HH:MM:SS`
* `LOG LEVEL` - Log level, possible values are:
    * `INFO` - Information
    * `WARN` - Warning
    * `ERROR` - Error
* `THREAD` - The name of the thread, module, plugin, etc., which has generated that log line. May absent, if output device can not print enough characters per line.

If output device support color, the line must be colored blue, yellow or red for information, warning or error log level respectively.
## Example
```
[2019-05-05 10:01:54][INFO][MAIN] Web server started
[2019-05-05 10:02:31][INFO][SERVER] Client 192.168.1.123 connected
[2019-05-05 10:02:32][WARN][SERVER] Client uses old protocol version, some methods can be unavailable
[2019-05-05 10:04:43][INFO][SERVER] Client connection closed
[2019-05-05 10:12:03][INFO][MAIN] Server stopped
```
