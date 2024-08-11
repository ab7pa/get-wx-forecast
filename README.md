# Get Current NWS Forecast for a Zone
## National Weather Service Forecast by Zone

This package adds a program to ``/etc/cron.hourly`` which will query the National Weather Service API for a 
specific *Zone* every hour. It overwrites the /www/wx-forecast.html file with the current weather forecast. 
You can find your local NWS *Zone* by searching at the following URL: https://alerts.weather.gov

To set the NWS zone, login to your node at the command line and edit the ``/etc/cron.hourly/get-wx-forecast`` 
file. Change the ``wx_zone`` variable to your NWS *Zone* identifier. This program assumes your node has Internet 
access on its WAN. On your node you can define a new service which points to your node:
http://<your node name>.local.mesh:80/wx-forecast.html

