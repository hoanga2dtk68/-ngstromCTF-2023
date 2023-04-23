# Simon Says
code để giao tiếp với server và trả lời với mỗi input cho
![image](https://user-images.githubusercontent.com/110059218/233826514-36375a3c-4531-420f-8280-1675835cf192.png)

import socket
import sys

HOST = 'challs.actf.co'
PORT = 31402

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    while True:
        data = s.recv(1024)
        response = data.decode().strip()
        print(response)
        words = response.split()
        if(len(words) == 0):
            continue
        p = words[6][:3]
        q = words[13][-3:]
        result = p + q + '\n'
        print(result)
        s.sendall(result.encode())

Server sẽ ngẫu nhiên gửi khoảng trắng hoặc flag bấm vài lần run code sẽ ra flag
![image](https://user-images.githubusercontent.com/110059218/233826582-e8ecf747-7982-48a9-b035-1ffb5e028077.png)
flag: actf{simon_says_you_win}
