# Monitor LUX in a UI using OpenSignals Node-RED TCP / IP flow

This example showcases how a specific channel can be monitored and make use of Node-RED's user interface **dashboard** to access real-time vizualisation of data. 
You'll need to configure your device MAC address in the filtering and printing within the flow.  
This is the case of the switch and the 2 nodes connected to it. 

## Prerequisites  
[Node-RED Dashboard](https://github.com/node-red/node-red-dashboard) (see LICENSE.md)  

## Steps  
[1. Example Flow](#flow)  
[2. Description](#desc)  

##  1. Flow and UI <a name="flow"></a>  
### Downloadable JSON
[OpenSignals TCP / IP flow](/LUX_ui/OS_TCP_LUX_ui.json)  

### Interface
![LUX UI FLow](LUX_mon_flow.png "OpenSignals TCP LUX UI Flow")

You should be able to see the following UI in your browser:
![LUX UI FLow](LUX_mon_ui.png "OpenSignals TCP LUX UI")


##  2. Description <a name="desc"></a>  
- Follow the [initial setup steps](https://github.com/malfarasplux/opensignals-nodered/#set)  
- Configure your MAC in the flow  
- Deploy, [launch the UI](http://localhost:1880/ui) and press start   
