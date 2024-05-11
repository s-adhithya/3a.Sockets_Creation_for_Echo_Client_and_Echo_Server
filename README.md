# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())  

```
### Server
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
## OUPUT
### Client
![329763593-1295284d-c30f-4ca6-9a16-404e6f78bedb](https://github.com/s-adhithya/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497423/6bcaf2e4-031d-490d-82d8-9c37885b98f7)

### Server
![329763600-a55a20de-d10a-44b5-8211-d463fb79fca4](https://github.com/s-adhithya/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497423/4fd07d98-ad37-4dfd-aabc-e9303042f562)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
