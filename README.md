This is a simple LabView client that works with Easy-Phi system.
Client uses REST API to communicate with the system. Client contains two basic use cases 
- send SCPI command to a particular module, addressed with SlotID; and query generic rack info.


Set up
———————
- Install LabView 2014
- Create a new LabView project (File->New project)
- Import send_scpi.vi and rack_info.vi (File->Open) 
- Open and run corresponding module

send_scpi.vi
—————

Input: 
Host - host ip address + port (Example: “http://127.0.0.1:8000”)
Slot - slot id of the module (Example: “1”)
SCPI - SCPI command to send (Example: “*IDN?”)

Output: 
Response - response from module

rack_info.vi
—————

Input:
Host - host ip address + port (Example: “http://127.0.0.1:8000”)

Output: 
Response - response from the system containing platform info

WebSockets support
—————
It is possible to create a LabView client that would support system’s WebSockets capabilities. 
However, at the moment there are no free-of-charge LabView addons with WebSockets client-side support. 
One potential LabView addon that supports WebSocket client-side capabilities can be found here:
http://www.lvs-tools.co.uk/software/websocket_api_for_labview/
