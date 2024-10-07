# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
```
NAME : ARSHITHA MS
REGISTER NUMBER : 212223240015
```
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

## SERVER:
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

## OUPUT
## CLIENT
<img width="960" alt="3bc" src="https://github.com/user-attachments/assets/841ca068-94da-48dd-baa6-9164a680fd4d">

## SERVER
<img width="960" alt="3bs" src="https://github.com/user-attachments/assets/767978bf-e4f1-4069-8b4c-c43dd563ae9a">

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
