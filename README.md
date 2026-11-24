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
## SERVER
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
## CLIENT
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

## OUPUT
<img width="448" height="157" alt="Screenshot 2026-11-24 101117" src="https://github.com/user-attachments/assets/625632ed-d122-4183-a62c-8c030fa36931" />
<img width="482" height="199" alt="image" src="https://github.com/user-attachments/assets/73126a82-8b4a-4101-ae53-0c70e3c10626" />


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
