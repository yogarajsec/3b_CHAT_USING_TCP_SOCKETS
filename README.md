# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Yogaraj.S 
## Reg no :212223040248
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
 ## client
 ```
 import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("client > ")
    s.send(msg.encode())
    print("server > ",s.recv(1024).decode())
```
 ## server
 ```
 import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUPUT
![Screenshot 2024-09-28 131956](https://github.com/user-attachments/assets/e25de882-8591-4ab5-b99a-04304ef5a443)
![Screenshot 2024-09-28 132011](https://github.com/user-attachments/assets/0372908f-9da6-47e7-b8f0-794b19a6f440)
## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
