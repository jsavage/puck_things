# puck_temp_mon was originally "puck_things" by koresar for which many thanks
# The following is based on content from http://forum.espruino.com/conversations/298104/#comment13400838
The intended use of this app was to monitor the temperature of an air conditioned office using a puck.js device

The Red LED flashes when the temperature gets 25º. The Blue LED flashes when it's 22º or lower.
If you click the Puck (button) the temperature monitoring will switch Off/On. If it blinks green on clicking - you turned the monitoring On.
To save some battery the temperature monitoring will turn Off automatically according to the schedule (time of the day and day of the week).

For simplicity the code assumes the Puck time zone is set to the local time (i.e. the local timezone is +00 hours). The author did it with the setTime function. Here is how to get a value for the setTime using node.js or a browser REPL: (Date.now() / 1000) + tzHours*60*60.

If you don't need the schedule feature, which relies on time, just remove the getTimeOfTheDay and resetScheduler functionality code lines 78-110  & line 112 where it is called.
