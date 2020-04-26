## mac配置多个ssh key

1. 进入ssh目录：
```
cd ~/.ssh
```

2. 创建新的ssh key：
```
ssh-keygen -t rsa -C "tigerhee@qq.com"
```

后续提示内输入name: id_rsa_tiger

3. 创建config文件：
```
touch config
```

配置config：

```
# github
Host git
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa

# github tiger
Host git2
HostName github.com
PreferredAuthentications publickey
User tigerhee@qq.com
IdentityFile ~/.ssh/id_rsa_tiger
```
4. 添加密钥：
```
ssh-add ~/.ssh/id_rsa_tiger
```

5. 到要用git2的仓库修改其git配置：

```
git config user.email "tigerhee@qq.com"
git config user.name "tigerHee"
```