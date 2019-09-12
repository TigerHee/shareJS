### 获取本地SSH Key：
```sh
  ls ~/.ssh

  cat ~/.ssh/id_rsa.pub
```

### 在远程仓库的master分支基础上建立新分支：
```
  git checkout master -b dev

  git push origin dev
```