<H1 ALIGN=CENTER> CREATION OF ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS </H1>
<H3> NAME : SHRRUTHILAYA G </H3>
<H3> REGISTER NUMBER : 212221230097 </H3>
<H3>EXPERIMENT NO : 03 A </H3>
<H3>DATE  : 11.05.2024 </H3>

## AIM:
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM:
1. Import the necessary modules in python.
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server .
4. Send and receive the message using the send function in socket.

## PROGRAM:
### CLIENT:
```PYTHON
import socket
s = socket.socket()
s.connect(('localhost',8000))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
```
### SERVER:
```PYTHON
import socket
s = socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c, addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUTPUT:
### CLIENT:
![client](https://github.com/Shrruthilaya-Gangadaran/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/93427705/046339bc-76bb-4d00-929d-436c774e4187)\

### SERVER:
![server](https://github.com/Shrruthilaya-Gangadaran/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/93427705/ab1123ca-706b-43d3-aa09-148e83d5f340)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.



