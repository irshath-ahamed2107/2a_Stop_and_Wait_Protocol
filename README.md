## Name: Irshath Ahamed.N
## Reg No: 212224110025
# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
### CLIENT: 
```
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
### SERVER:  
```
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT:
CLIENT 

![Image](https://github.com/user-attachments/assets/e7dcd5d6-2dc0-4341-a7d4-dcd24232da3a)

SERVER

![Image](https://github.com/user-attachments/assets/258e68da-4880-4e48-9f55-214315a33f1c)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.

