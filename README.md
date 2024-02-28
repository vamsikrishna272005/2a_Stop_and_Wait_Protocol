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
## PROGRAM
# CLIENT:-
```
import socket s=socket.socket() s.bind(('localhost',8000)) s.listen(5) c,addr=s.accept()
size=int(input("Enter number of frames to send: ")) l=list(range(size)) s=int(input("Enter Window
size:")) st=0 i=0
```
# SERVER:-
```
while True: Thus, python program to perform stop and wait protocol was successfully executed
while(i<len(l)): st+=s
c.send(str(l[i:st]).encode())
ack=c.recv(1024).decode()
if ack:
print(ack)
i+=s
```
## OUTPUT
# CLINT:-
![Screenshot 2024-02-28 015659](https://github.com/vamsikrishna272005/2a_Stop_and_Wait_Protocol/assets/147477015/8190c24c-883a-4004-81a3-496d2a80a051)
# SERVER:-
![Screenshot 2024-02-28 015717](https://github.com/vamsikrishna272005/2a_Stop_and_Wait_Protocol/assets/147477015/5a695c60-9288-4f91-a991-4cebacc4f566)
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
