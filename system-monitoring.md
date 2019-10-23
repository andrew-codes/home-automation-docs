# Monitoring the System Resources

## InfluxDB

Install [InfluxDB](https://github.com/hassio-addons/addon-influxdb) from hass.io community. This is a time-series database which can be used to query historical data; things like system monitoring, etc.

> Be sure to set a username and password in the configuration on the install page and set SSL to `false`.

Start the service and open the web UI. Create a new user for system-monitoring, `glances`, with a secure password. After creation, apply all permissions. Finally, be sure to create a glances database.

## System Monitoring via Glances

Install [Glances](https://community.home-assistant.io/t/community-hass-io-add-on-glances/97102) to monitor NUC’s resources. In the configuration section of the installation page, add information for the database, username, and password created above. Start the service, then open the web UI. The web UI will show you the current system monitoring.

You can use the InfluxDB's web UI to explore various fields and measurements over time.
