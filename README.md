## EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER
### DATE :24-04-2023

### AIM :

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

### ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server.
4.Send and receive the message using the send function in socket.
```
### PROGRAM :
```
Developed By: Silambarasan K
Reg No: 212221230101
```
### CLIENT :
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER :
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
### OUTPUT :

### CLIENT :

![image](https://user-images.githubusercontent.com/122860624/243070699-63f319b0-03af-4b86-8805-b267d1604c29.png)

### SERVER :

![image](https://user-images.githubusercontent.com/122860624/243070721-b7adbd32-4954-46ad-82f8-8153a45b0009.png)

### RESULT :

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
