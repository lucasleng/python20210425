```python
Asscii碼
a=[66,114,101,97,107,65,76,76,67,84,70,123,65,109,118,48,117,68,121,101,114,118,80,116,109,86,114,57,83,83,83,75,125]
>>> for i in a:
...     print(chr(i),end='')
![](https://raw.githubusercontent.com/MyFirstSecurity2020/HappyLinuxDay/main/%E8%B3%87%E5%AE%89%E5%AE%A3%E8%A8%80.GIF)

hello world

from pwn import *

ip="120.114.62.214"
port = 2400

r=remote(ip, port)
 
r.recvuntil("Now You Turn")
r.recvuntil(" : ")
res = r.recvline()[:-1]
res = list(map(int, res.split()))
res.sort()
r.recvuntil("answer :")
r.sendline(str(res[-3]))

r.interactive()

3rd

from pwn import *

ip="120.114.62.214"
port = 2403

r=remote(ip, port)

for i in range(1, 101):     
        r.recvuntil("wave")
        r.recvuntil("?")
        r.sendline(str(i))

r.interactive()  

```





