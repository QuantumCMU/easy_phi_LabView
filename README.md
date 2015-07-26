This is a simple LabView client that works with Easy-Phi system.
Client uses REST API to communicate with the system. Client contains two basic use cases: 
send SCPI command to a particular module, addressed with SlotID; and query generic rack info.


<h1>Set up</h1>

- Install LabView 2014
- Create a new LabView project (File->New project)
- Import send_scpi.vi and rack_info.vi (File->Open) 
- Open and run corresponding module

<h1>send_scpi.vi</h2>

Input: 
Host - host ip address + port (Example: “http://127.0.0.1:8000”)
Slot - slot id of the module (Example: “1”)
SCPI - SCPI command to send (Example: “*IDN?”)

Output: 
Response - response from module

<h1>rack_info.vi</h1>

Input:
Host - host ip address + port (Example: “http://127.0.0.1:8000”)

Output: 
Response - response from the system containing platform info

<h1>WebSockets support</h1>

It is possible to create a LabView client that would support system’s WebSockets capabilities. 
However, at the moment there are no free-of-charge LabView addons with WebSockets client-side support. 
One potential LabView addon that supports WebSocket client-side capabilities can be found here:
http://www.lvs-tools.co.uk/software/websocket_api_for_labview/
