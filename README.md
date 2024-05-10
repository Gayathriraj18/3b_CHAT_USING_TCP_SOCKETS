# 3b.CREATION FOR CHAT USING TCP SOCKETS

# Name : Gayathri A
# RegNo: 212221230028

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM :
# Client:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```

# Server:
```

import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUTPUT:

# Client :

![image](https://github.com/Gayathriraj18/3b_CHAT_USING_TCP_SOCKETS/assets/94154854/a227a90b-410b-4342-9209-04fb6bf17b3f)

# Server ;

![image](https://github.com/Gayathriraj18/3b_CHAT_USING_TCP_SOCKETS/assets/94154854/c0c7e201-1010-40f0-b3af-1f206f53c14f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
