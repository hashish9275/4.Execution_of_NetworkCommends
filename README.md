# 4.Execution_of_NetworkCommands
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

## PROGRAM:
Developed by:K.R.Hashish Vidya Sagar

Register Number: 212222230047

##PING COMMAND
## Client:
```
import socket 
from pythonping import ping 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    hostname=c.recv(1024).decode() 
    try: 
        c.send(str(ping(hostname, verbose=False)).encode()) 
    except KeyError: 
        c.send("Not Found".encode())
```
## Server:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
## Tranceroute command:
```
from scapy.all import* 
target = ["www.google.com"] 
result, unans = traceroute(target,maxttl=32) 
print(result,unans)

```


## Output:
##PING COMMAND
## CLIENT:
![image](https://github.com/anbuvinotha/4.Execution_of_NetworkCommends/assets/144871822/590b052c-abb5-41c2-8f61-bb4d8c291512)

## SERVER:
![image](https://github.com/anbuvinotha/4.Execution_of_NetworkCommends/assets/144871822/4ae6d86f-de51-498b-8ff4-22e856ef992c)

## TRANCEROUTE COMMAND:
![image](https://github.com/anbuvinotha/4.Execution_of_NetworkCommends/assets/144871822/0c5a071e-ef9b-4724-b472-b08163eca4d1)


## Result
Thus Execution of Network commands Performed 
