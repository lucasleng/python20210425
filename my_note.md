```python
base64編碼
happyhackinghighhaaha => aGFwcHloYWNraW5naGlnaGhhYWhh
連結:http://www.hipenpal.com/tool/base64-encode-and-decode-in-traditional-chinese.php

Base64
QnJlYWtBTExDVEZ7NTN1c1pRM2hXVzI1ZGNoWjdkWGV9 => BreakALLCTF{53usZQ3hWW25dchZ7dXe}
連結:http://www.hipenpal.com/tool/base64-encode-and-decode-in-traditional-chinese.php

Asscii碼
a=[66,114,101,97,107,65,76,76,67,84,70,123,65,109,118,48,117,68,121,101,114,118,80,116,109,86,114,57,83,83,83,75,125]
>>> for i in a:
...     print(chr(i),end='')
![](https://raw.githubusercontent.com/MyFirstSecurity2020/HappyLinuxDay/main/%E8%B3%87%E5%AE%89%E5%AE%A3%E8%A8%80.GIF)

Base32
IJZGKYLLIFGEYQ2UIZ5TS6BUHA2VMUZXO5UWS5CCLJMFKVLIJVSX2=== => BreakALLCTF{9x485VS7wiitBZXUUhMe}
連結:https://www.qqxiuzi.cn/bianma/base.php

Morse code
.. -. ..-. --- ... . -.-. ..-. .-.. .- --. .. ... -- --- .-. ... .. -. --. => INFOSECFLAGISMORSING
連結:https://mathsking.net/morse.htm

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





