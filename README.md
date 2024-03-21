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
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
address={"165.165.80.80":"6A:08:AA:C2","165.165.79.1":"8A:BC:E3:FA"};
while True:
    ip=c.recv(1024).decode()
    try:
        c.send(address[ip].encode())
    except KeyError:
        c.send("Not Found".encode()) 
```
### Server
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    ip=input("Enter logical Address : ")
    s.send(ip.encode())
    print("MAC Address",s.recv(1024).decode())
```
## OUPUT
### Client
![Screenshot 2024-03-21 152356](https://github.com/s-adhithya/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497423/fcb5b039-b510-441f-b382-bebf8b17bbe9)
### Server
![Screenshot 2024-03-21 152341](https://github.com/s-adhithya/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/113497423/ba13f257-9e8d-46bc-a7f2-3ae90483de44)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
