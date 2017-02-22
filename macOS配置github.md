##  git的安装与配置
### 1. 安装git
默认安装路径：/usr/local/git/bin/

### 2. 注册git项目托管网站：github

### 3. 配置git和github
1. 创建ssh密钥  

打开终端，执行：
```
$ cd ~/.ssh // 检查ssh密钥
```
如果没有提示:No such file or directory，说明不是第一次使用git,执行下面的操作,清理原有ssh密钥
 ```
 $ ls 
 config id_rsa id_rsa.pub  known_hosts //密钥文件名均以rsa结尾
 $ mkdir key_backup
 $ cp id_rsa* key_backup
 $ rm id_rsa*
 ```
 创建密钥：
 ```
 ssh-keygen -t rsa -C "defnngj@gmail.com"  //填写email地址，然后一直“回车”
 ```
 打开本地..\.ssh\id_rsa.pub文件。此文件里面内容为刚才生成的密钥

2. 为github添加密钥
 
登陆github系统，点击右上角`Settings>SSH and GPG keys> New SSH keys`，将本地生成的密钥复制到里面

3. 打开终端，测试链接是否成功
```
$ ssh -T git@github.com
```
如提示：
`*** You've successfully authenticated, but GitHub does not provide shell access.` 说明连接成功。  
如果看到：`The authenticity of host 'github.com (207.97.227.239)' can't be established.RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.Are you sure you want to continue connecting (yes/no)?`输入“yes”回车即可。

4. 设置用户信息  
```
$ git config --global user.name "***"   //给自己起个用户名
$ git config --globla user.email  "***@gmail.com"   //填写自己的邮箱
```

5. 创建token赋予权限
登陆github，找到`Settings>Personal access tokens>Create new token`，选择相应权限，创建token。  
打开终端：
```
$ git config --global github.user ***     //github 上的用户名
$ git config --globla github.token e97279836f0d415a3954c1193dba522f //创建的token
```


