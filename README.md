# EX.NO.2A - STOP AND WAIT PROTOCOL
## AIM :
To write a python program to perform stop and wait protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:

## Client:
```
VASANTH P
212222040175

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
```
## Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT:
## Client:
![WhatsApp Image 2024-04-30 at 22 26 20_34dd8492](https://github.com/JAYASREE24032006/2a_Stop_and_Wait_Protocol/assets/144360800/babac62c-b063-41e0-aaf6-6977a82f5175)

## Server:
![WhatsApp Image 2024-04-30 at 22 26 43_6241820c](https://github.com/JAYASREE24032006/2a_Stop_and_Wait_Protocol/assets/144360800/1ddd6c66-b581-416b-8c3f-a75f6afc22cd)

## RESULT:
Thus, python program to perform stop and wait protocol was successfully executed.
