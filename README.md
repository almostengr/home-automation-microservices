# Home Automation Microservices

This project originaly was for internet monitor. It has expanded to be a microservices platform 
that integrates with Home Assistant for home automation. Several IOT devices have web interfaces, such as 
routers, but do not have APIs. Thus this API was created so that an API could be called by the home 
automation system, to perform tasks that via the device's HTML interface.

## Internet Monitor

Reboots the DD-WRT router when there are no WiFi clients connected to it.

### Problem

My router would occasionally disconnect any of the wireless clients that were connected to it. Since
I have wired and wireless devices connected, some of the time I would not know that the wifi had
stopped working until my phone or laptop wouldn't connect or I noticed that a automation did not
trigger when it should have.

## Solution

After updating to the latest DD-WRT firmware, the problem persisted.  Given that I work building
automations to improve business processes, I decided that I would build and automation that would
connect to the router’s web interface and see if there are any wireless clients connected to it.
If there are no connected wireless clients, then there is a great chance that the wifi process that
authenticates clients has crashed.  As a result, the process would need to be restarted and the easiest
way to restart the process would be to reboot the router.

## Project Information

For more information about this project and help documentation, visit 
[https://thealmostengineer.com/internetmonitor](https://thealmostengineer.com/internetmonitor).

## HD Home Run 

### Problem

HD HomeRun would receive updates via the web and display a notification on the UI of the device. Only problem 
is that I rarely access the web UI of the devices.

### Solution 

Create a Selenium automation that is triggered by an API call from the home automation or other system. This 
will perform the task such as installing pending updates or checking the status of the tuners.
