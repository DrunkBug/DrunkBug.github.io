# 
## 生成密钥
-  `C:\Users\xxx\.ssh\` 目录下生成密钥  
```cmd
    ssh-keygen -t rsa -C 
```
## github配置文件
- ssh配置中New SSH key，将生成将id_rsa内容复制其中。 
## 本地ssh配置文件
- 文件 `C:\Users\xxx\.ssh\config`
-  github上个人ssh配置中New SSH key
```conf
#ProxyCommand connect -H xxx.xxx.xxx.xxx:xxxx -a none %h %p
# -H http代理， -S socks代理，-T tcp代理
Host github.com
  User git
  Port 22
  Hostname github.com
  # 注意修改路径为你的路径
  IdentityFile "C:\Users\admin\.ssh\id_rsa"
  TCPKeepAlive yes
Host ssh.github.com
  User git
  Port 443
  Hostname ssh.github.com
  # 注意修改路径为你的路径
  IdentityFile "C:\Users\admin\.ssh\id_rsa"
  TCPKeepAlive yes
```