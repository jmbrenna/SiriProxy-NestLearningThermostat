SiriProxy-NestLearningThermostat
================================
About
-----
Plugin for SiriProxy to communicate with the Nest.com servers to set thermostat temperature or get the status of the thermostat.
This plugin requires a nest.com account and Nest hardware from http://www.nest.com/

This plugin was adapted from SiriProxy-Thermostat plugin to call into nest.com.

Important Note, this plugin is neither developed, nor endorsed by nest.com, do not contact them about problems or issues you encounter with this plugin. 

If you're having problems with the plugin, open an issue on github.

Config
------
Copy config-info.yml into ~/.siriproxy/config.yml and edit as appropriate. 

Usage
-----
Say things like:

* 'Set the thermostat to 65 degrees'
* 'Set the nest to 65'
* 'What's the status of the nest'
* 'What is the status of the thermostat'
* 'Set the nest to away'
* 'Set the thermostat to away'
* 'Let the nest know that I'm home'

Background
----------
Connected my iPhone to a Paros proxy running on my mac (http://www.parosproxy.org/).
I then ran the nest iPhone app to analyze the request/response interactions. 

My HVAC setup is a single-stage heating (Rc,W) so if you have heating/cooling combination or other factors, the responses from nest.com maybe a little different and would have to be modified slightly: Namely to send an appropriate command to toggle between heat/cool/fan etc.
The only option I had using the nest app was to send a target temperature, not an HVAC mode such as heat/cool/fan.


Examples
-------

* https://twitter.com/#!/the_chilitechno/status/142988344941486080/photo/1
* https://twitter.com/#!/the_chilitechno/status/143031527821938688/photo/1

Caveats
-------
* Currently only works with a single nest thermostat. I don't have multiple thermostats installed so it's hard to test, but should be relatively easy to adapt.
* I tried getting Siri to understand 'Check the status of the Nest' but it kept saying it couldn't look up flight information. This seems to be sporadic because sometimes Siri reads 'Nest' as 'next'
* I developed this on my home HVAC system which only has single-stage heating (Rc, W) so your mileage may vary if you have a different setup and you'll likely need to further analyze the nest iPhone app request/response stream.

To Do
-----
* Caching of authentication token (currently logs into nest for each request)
* Caching of device information 
* Support heat / cooling

Licensing
---------

Re-use of my code is fine under a Creative Commons 3.0 [Non-commercial, Attribution, Share-Alike](http://creativecommons.org/licenses/by-nc-sa/3.0/) license. In short, this means that you can use my code, modify it, do anything you want. Just don't sell it and make sure to give me a shout-out. Also, you must license your derivatives under a compatible license (sorry, no closed-source derivatives). If you would like to purchase a more permissive license (for a closed-source and/or commercial license), please contact me directly. See the Creative Commons site for more information.

