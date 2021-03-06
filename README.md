# VolkswagenID3-widgets
Some useful widgets based on iobroker

To install:

1. Install iobroker from here: https://www.npmjs.com/package/iobroker.js-controller
2. Add the we.connect plugin from here: https://github.com/ta2k/ioBroker.vw-connect/blob/master/README.md
3. Enter your volkswagen.id credentials (username, password and, if you have it, your s-pin). Note you need to select "ID" not "VW" in the adapter settings.
4. Install the vis-inventwo widget set in the adapter menu of iobroker
5. Install the vis (visualization) adapter
6. Deploy the javascript code for the charging menu and the scheduler in the scripts section
7. Create the user variables in 0_userdata.0 as listed in the javascript code 

Note: you must install the vw-connect plugin with the little github icon in the adapter menu of iobroker in order to get the latest version since the code is under development.

The scheduler checks every minute if:
- the timer for charging was set
- if an error in the server communication occured and sends a push notification to a pushsafer defined device
- if charging was started from the ConnectID app

In order to enable push notifications, you need to install the following iobroker plugins:
1. pushsafer (follow the instructions with the pluging to enable notifications to your devices)
2. logparser and configure it according to the instructions to search for error messages in the logfile

Then you may import the views and the corresponding js code. 
Ensure that you adopt the VIN placeholder with your VIN in the code.

The images directory includes screenshots of the different menus and the pushsafer notification in an Apple Watch

Known issues:
- With the id3 software version 0564, the climatisation parameters can be displayed but not set (appears to work with 0784 according to other users)

### Please note: This is all experimental, not endorsed by Volkswagen, and to be used at your own risk.
