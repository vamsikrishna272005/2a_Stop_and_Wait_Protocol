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
# SERVER:-
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recieved".encode())
```
## OUTPUT
# CLINT:-
![Screenshot 2024-03-05 154139](https://github.com/vamsikrishna272005/2a_Stop_and_Wait_Protocol/assets/147477015/a39d0847-f15e-463f-9356-00c0c40ca10c)
# SERVER:-
![Screenshot 2024-03-05 154156](https://github.com/vamsikrishna272005/2a_Stop_and_Wait_Protocol/assets/147477015/39f6cffa-fa72-4ef0-b26f-09f44af81c9b)
![Screenshot 2024-03-05 154247](https://github.com/vamsikrishna272005/2a_Stop_and_Wait_Protocol/assets/147477015/a487ccd0-d297-4f74-b511-4ad95c7a35e5)
## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
