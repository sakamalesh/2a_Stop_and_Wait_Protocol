# 2a_Stop_and_Wait_Protocol
## Name:Kamalesh
## Reg No:212223040083
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


## Client:
'''

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
'''

## Server:

'''

    import socket
    s=socket.socket()
    s.connect(('localhost',8000))
    while True:
     print(s.recv(1024).decode())
     s.send("Acknowledgement Recived".encode())

'''
## OUTPUT
## Client
![Screenshot 2024-09-14 102848](https://github.com/user-attachments/assets/4f83b80a-41e5-4e02-8a50-8c5d6c6fa169)

## Server:
![Screenshot 2024-09-14 102910](https://github.com/user-attachments/assets/1b4b58bc-02ee-42e7-9ede-8b61666befb5)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
