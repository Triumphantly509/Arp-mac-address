# Arp-Mac-Address
### Diagram
<img width="742" height="448" alt="image" src="https://github.com/user-attachments/assets/7bb70007-5e88-4516-a3fc-7f27851f43b7" />

### Arp cache of PC2
<img width="449" height="136" alt="image" src="https://github.com/user-attachments/assets/a3382f84-912f-4013-a2a8-e18721b17896" />

### Filter only for ARP
<img width="313" height="504" alt="image" src="https://github.com/user-attachments/assets/d84e152f-98ae-428a-b0ee-9a6da545958c" />

### PC2 pings PC0
<img width="659" height="654" alt="image" src="https://github.com/user-attachments/assets/d5a2ffa2-0094-40e7-a396-7fbf2ca70644" />

### Simulation panel from Packet Tracer
<img width="725" height="189" alt="image" src="https://github.com/user-attachments/assets/75ed3b54-4fd4-4500-9562-74ef90d256ea" />

### Explanation
PC2 constructs an ARP request from Src-IP: 192.168.1.1 to FFFF (broadcast to the local area network) and it needs to know the Mac-address for the device with IP-add: 192.168.1.3

### From the switch perspective
<img width="708" height="558" alt="image" src="https://github.com/user-attachments/assets/eefe4583-1979-419f-b136-12e5d8a40643" />
It receives the broacast frame from PC2

Then it floods it out its other ports.

It sends one copy to PC0 and PDC1
<img width="781" height="185" alt="image" src="https://github.com/user-attachments/assets/52ccd54d-4569-4df7-9bca-0463169fa00c" />

PC1 receives the broadcast frame, since it does have such IP address, it does not reply, that is why only inbound PDU is seen here no reply, no outbound PDU, refer to the snapshop below.

<img width="542" height="506" alt="image" src="https://github.com/user-attachments/assets/43960952-da9e-42ed-b74d-d8ac4b68875b" />

PC0 understands the ARP Request is asking for it's IP address, it replies by an ARP REPLY, (UNICAST)
<img width="544" height="506" alt="image" src="https://github.com/user-attachments/assets/af32214f-52c6-4aa4-86bd-2c8b2cdf07ea" />

Finally the switch receives the frame from pc0 via its port fastethernet 0/1 then send it to PC2.

### Result
Arp cache from PC2
<img width="456" height="84" alt="image" src="https://github.com/user-attachments/assets/52dc61e0-596b-4d8f-b7a9-5978af12f063" />

