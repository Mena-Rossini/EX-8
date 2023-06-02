# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE : 24-04-2023

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM :
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it will send NACKsignal to client.
6. Stop the program

## PROGRAM :

### CLIENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())

 ```
### SERVER :
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   c.send(ClientMessage.encode())
 ```
## OUTPUT :
### CLIENT :
![241380995-d7dd9d06-1e79-4bca-b7dc-d3dc7daabece](https://github.com/Mena-Rossini/EX-8/assets/102855266/aced70bf-a236-4b04-9500-348d5e6e629c)


### SERVER :

![241381010-b08b7e8a-5f67-4a15-bafa-63b05e9d14e5](https://github.com/Mena-Rossini/EX-8/assets/102855266/9cd7ad35-081b-4256-ba92-2dbd55219798)

## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed
