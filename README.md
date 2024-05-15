# 4a.Execution_of_NetworkCommands
## AIM :Use of Network commands in Real Time environment
## Software : Command Prompt And Network Protocol Analyzer
## Procedure: To do this EXPERIMENT- follows these steps:
<BR>
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer 
<BR>
All commands related to Network configuration which includes how to switch to privilege mode
<BR>
and normal mode and how to configure router interface and how to save this configuration to
<BR>
flash memory or permanent memory.
<BR>
This commands includes
<BR>
• Configuring the Router commands
<BR>
• General Commands to configure network
<BR>
• Privileged Mode commands of a router 
<BR>
• Router Processes & Statistics
<BR>
• IP Commands
<BR>
• Other IP Commands e.g. show ip route etc.
<BR>

## PROGRAM
## CLIENT:
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost'8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
## SERVER:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
## OUTPUT
## PING COMMAND:
## CLIENT:
![328130287-7ec5e120-f679-4153-82b2-9e19c0d4c0ee](https://github.com/sriharan23000516/4.Execution_of_NetworkCommends/assets/139841769/a145958f-0937-4f99-9ded-bb184c0936f8)


## SERVER:
![328130315-ea7f639d-c8c3-41d4-8bed-441f05587f59](https://github.com/sriharan23000516/4.Execution_of_NetworkCommends/assets/139841769/dfbe4d10-cc7b-41f0-adc2-6d3b21179b93)


## TRACERT COMMAND:
![328130334-ff4a6e87-618e-429f-b6eb-9bbe388264d1](https://github.com/sriharan23000516/4.Execution_of_NetworkCommends/assets/139841769/ef3cf83e-5eff-4ad0-a51d-0c96fbfec7a0)


## Result
Thus Execution of Network commands Performed.
