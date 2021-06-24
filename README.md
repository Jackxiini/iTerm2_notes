# iTerm2 Session共享

当前登录远程服务器后，新开窗口还需要重新输入密码登录，十分麻烦， 但是我们可以通过配置 ~/.ssh/config 文件可达到 session 共享的目的。

编辑或创建 ~/.ssh/config 文件，输入如下内容：

```
Host *
  ControlMaster auto
  ControlPath ~/.ssh/%r@%h:%p
```

保存后再次登录机器，新开窗口中执行 ssh 登录无需再次输入密码，可直接登入。
