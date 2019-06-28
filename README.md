# OpenSignals Node-RED TCP / IP flow

[1. Prerequisites](#req)  
[2. Setup](#set)  
[3. Flow](#flow)  
[4. Troubleshooting](#ts)  


##  1. Prerequisites <a name="req"></a>
[Node-RED](https://nodered.org/)  
[PLUX OpenSignals](https://bitalino.com/en/software)  

##  2. Setup <a name="set"></a>
1. Launch OpenSignals and configure the TCP/IP Save Integration with the chosen port
![OS_TCP Setup](/img/OS_TCP.png "OpenSignals TCP Configuration")

2. Launch Node-RED and import the flow from clipboard or JSON file

3. Deploy your flow

4. Click on the Start Node and begin receiving your sensor data. You're ready to see it in the debug window or process it as you like

##  3. Flow <a name="flow"></a>
[OpenSignals TCP / IP flow](/flow/opensignals_tcp.json)  
![OS_TCP_flow](/img/OS_TCP_flow.png "OpenSignals TCP Flow")

##  4. Troubleshooting <a name="ts"></a>
In case the default port 5555 is busy, you will likely receive an error message that will break the TCP connection.
![OS_TCP_port_error](/img/ts_OS_TCP_porterr.png "OpenSignals TCP port error")

Try assigning another port, e.g. 3003, in the TCP node in the flow and deploying. The given port must match the OpenSignals one.
![OS_TCP_port_error_flow](/img/ts_OS_TCP_porterr_flow.png "Assigning a different TCP port")
