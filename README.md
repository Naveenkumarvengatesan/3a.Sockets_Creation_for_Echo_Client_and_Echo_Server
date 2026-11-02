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

Server:

~~~
import socket

with socket.socket() as s:
    s.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR, 1)
    s.bind(('localhost', 8001))
    s.listen(5)
    c, addr = s.accept()
    print("Connected:", addr)
    with c:
        while data := c.recv(1024):
            c.sendall(data)
~~~

Client:

~~~
import socket

with socket.socket() as s:
    s.connect(('localhost', 8001))
    while (msg := input("Client > ")) != "exit":
        s.sendall(msg.encode())
        print("Server >", s.recv(1024).decode())
~~~
## OUTPUT
<img width="1275" height="317" alt="image" src="https://github.com/user-attachments/assets/01d40b3e-85aa-4181-9ca2-7df51f255ac2" />



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
