# 4.Execution_of_NetworkCommands
# NAME:R.MUSHAFINA
# REGISTER NUMBER:212224220067
# AIM:
Use of Network commands in Real Time environment
# SOFTWARE:
Use of Network commands in Real Time environment
# PROCEDURE: 
# To do this EXPERIMENT- follows these steps:
In this EXPERIMENT- students have to understand basic networking commands e.g cpdump, netstat, ifconfig, nslookup ,traceroute and also Capture ping and traceroute PDUs using a network protocol analyzer
All commands related to Network configuration which includes how to switch to privilege mode
and normal mode and how to configure router interface and how to save this configuration to
flash memory or permanent memory.
This commands includes
• Configuring the Router commands
• General Commands to configure network
• Privileged Mode commands of a router
• Router Processes & Statistics
• IP Commands
• Other IP Commands e.g. show ip route etc.

# PROGRAM:
```
CLIENT: 
 
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
 
SERVER: 
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    ip=input("Enter the website you want to ping ") 
    s.send(ip.encode()) 
    print(s.recv(1024).decode())
```
# OUTPUT:
![image](https://github.com/user-attachments/assets/733d3f0b-da31-4b43-bea0-9d1cd49a4cf6)
![image](https://github.com/user-attachments/assets/67773fcb-f6da-40d7-991c-bdec984db1cb)

# RESULT:
Thus Execution of Network commands Performed

