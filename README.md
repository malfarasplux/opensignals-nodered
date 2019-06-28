# OpenSignals Node-RED TCP / IP flow

[1. Prerequisites](#req)  
[2. Setup](#set)  
[3. Flow](#flow)  

##  1. Prerequisites <a name="req"></a>
[Node-RED](https://nodered.org/)  
[PLUX OpenSignals](https://bitalino.com/en/software)  

##  2. Setup <a name="set"></a>
1. Launch OpenSignals and configure the TCP/IP Save Integration with the chosen port
![OS_TCP Setup](/img/OS_TCP.png "OpenSignals TCP Configuration")

2. Deploy your flow
3. Click Start

##  3. Flow <a name="flow"></a>
```javascript
[
    {
        "id": "657b7a1f.2f7664",
        "type": "tab",
        "label": "OpenSignals TCP",
        "disabled": false,
        "info": ""
    },
    {
        "id": "67cfc50c.cf83ac",
        "type": "comment",
        "z": "657b7a1f.2f7664",
        "name": "OpenSignals TCP / IP",
        "info": "",
        "x": 240,
        "y": 80,
        "wires": []
    },
    {
        "id": "d398fec5.a4b3",
        "type": "tcp request",
        "z": "657b7a1f.2f7664",
        "server": "localhost",
        "port": "5555",
        "out": "sit",
        "splitc": " ",
        "name": "OpenSignals TCP / IP",
        "x": 460,
        "y": 220,
        "wires": [
            [
                "39a279f.d724386"
            ]
        ]
    },
    {
        "id": "af438436.7a8838",
        "type": "inject",
        "z": "657b7a1f.2f7664",
        "name": "",
        "topic": "",
        "payload": "start",
        "payloadType": "str",
        "repeat": "",
        "crontab": "",
        "once": false,
        "onceDelay": 0.1,
        "x": 250,
        "y": 160,
        "wires": [
            [
                "d398fec5.a4b3"
            ]
        ]
    },
    {
        "id": "5aae32bd.a85f0c",
        "type": "inject",
        "z": "657b7a1f.2f7664",
        "name": "",
        "topic": "",
        "payload": "stop",
        "payloadType": "str",
        "repeat": "",
        "crontab": "",
        "once": false,
        "onceDelay": 0.1,
        "x": 250,
        "y": 240,
        "wires": [
            [
                "d398fec5.a4b3"
            ]
        ]
    },
    {
        "id": "57dbf534.bef08c",
        "type": "debug",
        "z": "657b7a1f.2f7664",
        "name": "",
        "active": true,
        "tosidebar": true,
        "console": false,
        "tostatus": false,
        "complete": "true",
        "targetType": "full",
        "x": 850,
        "y": 220,
        "wires": []
    },
    {
        "id": "39a279f.d724386",
        "type": "function",
        "z": "657b7a1f.2f7664",
        "name": "JSON parse",
        "func": "p = JSON.parse(msg.payload);\nnode.log(typeof p);\nmsg.payload=p;\nreturn msg;",
        "outputs": 1,
        "noerr": 0,
        "x": 710,
        "y": 220,
        "wires": [
            [
                "57dbf534.bef08c"
            ]
        ]
    },
    {
        "id": "891933d1.08d22",
        "type": "comment",
        "z": "657b7a1f.2f7664",
        "name": "TCP (keep alive) request to port",
        "info": "",
        "x": 490,
        "y": 180,
        "wires": []
    }
];
```
