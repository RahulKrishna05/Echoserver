# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
server code:
```
import socket

s=socket.socket()

host=socket.gethostname()
port=1234

s.bind((host, port))

s.listen(5)

while True:
    conn, addr = s.accept()
    print("Got connection from :", addr)
    conn.send(b'Thank you for connecting')
    conn.close()
```
client code:
```
import socket

s=socket.socket()

host=socket.gethostname()
port=1234

s.connect((host,port))
print(s.recv(1024))
s.close()
```
## OUTPUT:
server output:
![Screenshot 2024-03-05 114353](https://github.com/RahulKrishna05/Echoserver/assets/162027231/0bc10081-5da8-4a7c-9be3-47f91088f293)
client output:
![Screenshot 2024-03-05 114407](https://github.com/RahulKrishna05/Echoserver/assets/162027231/cdbb2814-fc39-4ea1-ba43-258f5fe8568d)
## RESULT:
The program is executed successfully
