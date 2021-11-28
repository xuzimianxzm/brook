## Run Code

不需要安装任何brook 或 joker 的 cli工具,直接命令行运行代码。

### socks5 server

```shell
# 1. run socks5 server
go run ./cli/brook/. socks5 --socks5 127.0.0.1:8000

# 2. check socks5 server 
curl --socks5 127.0.0.1:8000 https://www.baidu.com/
```

### socks5tohttp

```shell
# 1. run socks5 server
go run ./cli/brook/. socks5 --socks5 127.0.0.1:8000

# 2. check socks5 server 
curl --socks5 127.0.0.1:8000 https://www.baidu.com/

# 3. run socks5tohttp server 
# brook socks5tohttp 可以将 socks5 proxy 转换为 http proxy. 假设你要将 socks5 proxy 127.0.0.1:1080 转换为 http proxy 127.0.0.1:8010
go run ./cli/brook/. socks5tohttp --socks5 127.0.0.1:8000 --listen 127.0.0.1:8010

# 2. check http server 
curl -x 127.0.0.1:8010 https://www.baidu.com/
```
