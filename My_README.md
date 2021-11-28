## Run Code

不需要安装任何brook 或 joker 的 cli工具
```shell
# run socks5 server
go run ./cli/brook/. socks5 --socks5 127.0.0.1:8000

# check socks5 server 
curl --socks5 127.0.0.1:8000 https://www.baidu.com/
```