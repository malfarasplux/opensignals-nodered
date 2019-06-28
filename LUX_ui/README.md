# Monitor LUX in a UI using OpenSignals Node-RED TCP / IP flow

This example showcases how a specific channel can be monitored and make use of Node-RED's user interface to access real-time vizualisation of data. 
You'll need to configure your device MAC address in the filtering and printing within the flow.  
[1. Flow](#flow)  
[2. Description](#desc)  

##  1. Flow and UI <a name="flow"></a>  
[OpenSignals TCP / IP flow](/OS_TCP_LUX_ui.json)  
![LUX UI FLow](LUX_mon_flow.png "OpenSignals TCP LUX UI Flow")

You should be able to see the following UI in your browser:
![LUX UI FLow](LUX_mon_ui.png "OpenSignals TCP LUX UI")


##  2. Description <a name="ts"></a>  
- Follow the [initial setup steps](https://github.com/malfarasplux/opensignals-nodered/)  
- Configure your MAC in the flow  
- Deploy, [launch the UI](http://localhost:1880/ui) and press start   
