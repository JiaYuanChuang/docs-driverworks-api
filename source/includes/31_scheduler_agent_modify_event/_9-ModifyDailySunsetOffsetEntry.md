## ModifyDailySunsetOffsetEntry

This API allows you to modify the Daily Sunset Offset Entry event. Use a negative number for before sunset and a positive number for number of minutes after sunset. Modifies the Event based on the Event ID passed. This API uses the parameters found in the  Daily Sunset Offset Entry API for convenience. A driver can only modify events which were created by that driver.

###### Available from 3.0.0


### Signature

`C4Scheduler:ModifyDailySunsetOffsetEntry(name, offset_minutes, start_time, end_date, options)`


| Parameter | Description |
| --- | --- |
| str | String value of the name of the event being modified. |
| table | offset minutes includes: number, number of minutes, range (-360 - 360) |
| table | start time includes year, month, day, hour using 24 hour clock. Minute is optional. The default time is 12:00 AM. |
| table | end date. optional. includes: year, month, day |
| table | Table of additional, optional parameters that includes: |
| | hidden - Boolean. Defaults to false. Setting to true prevents the Event from displaying in the Scheduler Agent in ComposerPro |
| | `user_hidden` - Boolean. Defaults to false. Setting user hidden to true prevents the Event from displaying on Navigators. |
| | category - String value that is available to the driver writer to use however they see fit. Can be used to categorize events. |
| | enabled - Boolean which defaults to true. Setting enabled to false will disable the Event. |
| | locked - Boolean which defaults to false. Setting enabled to true will place the Event in a read only state. |


### Returns

| Value | Description |
| --- | --- |
| True | Successful |
| False | Modification failed |